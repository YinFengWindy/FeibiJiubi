# feibi-jiubi-jimeng-video

一个面向即梦视频模式的 Codex Skill。

它专门处理这类需求：用户会上传参考图控角，希望把角色放进 `现实教室 / 房间 / 便利店 / 咖啡店 / 校园` 等环境里，做成以 `可爱动作、表情反应、镜头抓点` 为核心卖点的 `15 秒短视频`。重点不是剧情，而是动作是否一眼能懂、表情是否够甜、镜头是否能把记忆点拍清楚。

## 适合做什么

- 把一句话点子扩成即梦可用的视频提示词
- 重写“像图片、不像视频、没动作卖点”的失败草稿
- 先脑暴一波可爱动作方向，再扩成成品提示词
- 把环境从“背景名词”改成真正能承托动作的现实场景

## Skill 特点

- 默认按 `参考图控角` 使用，不重复堆角色外形
- 默认按 `15 秒` 节奏设计
- 优先做 `单动作主线 + 单情绪中心 + 单镜头逻辑`
- 环境只做承托，不默认走剧情
- 特别适合 `现实教室` 这类真实短视频感场景

## 安装

把仓库里的 `feibijiubi` 整个文件夹复制到 Codex 的技能目录：

### Windows PowerShell

```powershell
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE/.codex/skills" | Out-Null
Copy-Item -LiteralPath ".\feibijiubi" -Destination "$env:USERPROFILE/.codex/skills/feibijiubi" -Recurse -Force
```

### macOS / Linux

```bash
mkdir -p ~/.codex/skills
cp -R ./feibijiubi ~/.codex/skills/feibijiubi
```

目标目录应为：

```text
~/.codex/skills/feibijiubi/
├── SKILL.md
├── agents/openai.yaml
└── references/
```

## 使用示例

```text
使用 $feibi-jiubi-jimeng-video 基于我上传的参考图，给我几个以可爱动作为卖点的15秒视频方向，不要走剧情。
```

```text
使用 $feibi-jiubi-jimeng-video 把这条草稿重写成现实教室背景的即梦视频提示词，重点强化歪头、眨眼、甜笑这些动作记忆点。
```

```text
使用 $feibi-jiubi-jimeng-video 给我一个现实教室跳舞版，动作简单、短视频感强、镜头别太乱。
```

## 注意

- 技能目录名保持为 `feibijiubi`
- 复制时保留 `agents/` 和 `references/`
- 更新时建议整包覆盖
