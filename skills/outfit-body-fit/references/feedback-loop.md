# 反馈回填

没有回填，这个 skill 只能不断给出一套推理正确但未经检验的建议。回填是把「推理」变成「证据」的唯一途径。

## 存在哪

用户主目录下，**不在仓库里**：

- Windows：`%USERPROFILE%\.outfit-body-fit\`
- macOS / Linux：`~/.outfit-body-fit/`

仓库 `.gitignore` 已排除 `.outfit-body-fit/` 和 `*.jsonl`，不会误提交。

## 两个文件

### profile.json（可选）

长期画像。用户第二次来时不用重问一遍。

```json
{
  "measurements": {
    "height_cm": 170, "shoulder_width_cm": 36, "hip_width_cm": 38,
    "waist_cm": 72, "hip_cm": 94, "bust_cm": 87, "crotch_height_cm": 76
  },
  "computed": { "shr": 0.95, "whr": 0.77, "lbr": 0.45 },
  "constraints": { "no_heels": true, "budget": "中", "climate": "华东" },
  "known_good": ["正肩薄垫肩西装", "深灰直筒九分西裤"],
  "known_bad": ["插肩卫衣", "大摆伞裙"]
}
```

`known_good` / `known_bad` 是用户说过的、以及从 feedback 里累积的结论，不写推测。

### feedback.jsonl（每行一条）

```json
{"date":"2026-11-11","scenario":"通勤-会议","prescriptions":["正肩+方领","明度递进"],"worn":"米白正肩西装 + 深灰直筒 + 黑乐福","verdict":"好","note":"肩线明显改善，裤长偏长","reuse":true}
```

| 字段 | 取值 |
|---|---|
| `verdict` | `好` / `中` / `差` |
| `reuse` | `true`（会再穿）/ `false`（不会） |
| `note` | 一句话，≤30 字，写具体哪里对、哪里不对 |

`prescriptions` 要写处方标签，不要写整段话——后面统计靠它匹配。

## 怎么收集（不打扰）

方案输出末尾附一行：

> 穿完回一句就够：`好 / 中 / 差 + 一句话`

用户不回就算了，不追问第二次。

## 怎么用

**开场**：`profile.json` 存在就读，已知数据不再问；`feedback.jsonl` 存在就读最近 5 条。

**调处方**：

- 同一处方连续 2 次 `差` → 这条对这个用户不成立。改走「冲突调和」里的备选，并在输出里明说改了什么
- 同一处方累计 3 次 `好` → 提为默认动作，不再解释原理
- `reuse: false` 多于 `reuse: true` 的整套方案 → 整套降级，不再原样复用

**写回**：用户回填后立刻追加一行，并同步更新 `known_good` / `known_bad`。不要攒着等下次。

## 边界

- 只存文字结论，**不存照片**
- 不回填用户没说过的信息（比如体重、年龄、身材评价）
- 用户说删就删，不留备份
- 对外分享这个 skill 时，记录不会跟着走——它在用户自己机器上
