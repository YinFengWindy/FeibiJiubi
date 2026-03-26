# feibi-jiubi-jimeng-video

面向即梦视频模式的提示词优化与题材头脑风暴技能。

适用于用户会上传参考图控制角色形象时，将环境迁移类点子、已有草稿或失败案例，重写为更适合即梦的 15 秒视频提示词；也适合围绕菲比啾比题材做环境创意脑暴。

## 能力概览

- 环境设计
- 角色与场景的接触关系设计
- 15 秒视频节奏拆分
- 即梦视频提示词优化
- 菲比啾比题材脑暴
- 失败案例重写与修复

## 仓库结构

```text
.
├── README.md
└── feibi-jiubi-jimeng-video/
    ├── SKILL.md
    ├── agents/openai.yaml
    └── references/
```

安装时请复制整个 `feibi-jiubi-jimeng-video` 文件夹，不要只复制 `SKILL.md`。

## 安装方法

### 1. 克隆或下载仓库

```bash
git clone <your-github-repo-url>
cd <repo-folder>
```

也可以直接在 GitHub 页面下载 ZIP，解压后进入仓库目录。

### 2. 复制技能目录到 Codex 技能路径

#### Windows PowerShell

```powershell
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE/.codex/skills" | Out-Null
Copy-Item -LiteralPath ".\feibi-jiubi-jimeng-video" -Destination "$env:USERPROFILE/.codex/skills/feibi-jiubi-jimeng-video" -Recurse -Force
```

#### macOS / Linux

```bash
mkdir -p ~/.codex/skills
cp -R ./feibi-jiubi-jimeng-video ~/.codex/skills/feibi-jiubi-jimeng-video
```

### 3. 确认安装结果

安装完成后，目标目录应类似于：

```text
~/.codex/skills/feibi-jiubi-jimeng-video/
├── SKILL.md
├── agents/openai.yaml
└── references/
```

## 更新方法

当仓库内容更新后，重新拉取并覆盖技能目录即可。

#### Windows PowerShell

```powershell
git pull
Copy-Item -LiteralPath ".\feibi-jiubi-jimeng-video" -Destination "$env:USERPROFILE/.codex/skills/feibi-jiubi-jimeng-video" -Recurse -Force
```

#### macOS / Linux

```bash
git pull
cp -R ./feibi-jiubi-jimeng-video ~/.codex/skills/feibi-jiubi-jimeng-video
```

## 使用示例

安装完成后，可以直接这样触发：

```text
[$feibi-jiubi-jimeng-video](~/.codex/skills/feibi-jiubi-jimeng-video/SKILL.md) 头脑风暴
```

也可以直接用自然语言描述需求：

```text
使用 $feibi-jiubi-jimeng-video 基于我上传的参考图，脑暴几个偏可爱、卖萌、轻甜气质的 15 秒环境点子。
```

## 适合的使用场景

- 想把参考图角色放进教室、便利店、咖啡店、街道、异世界等环境
- 已有提示词草稿，但结果“像图片、不像视频、没短视频感”
- 想先脑暴几个可爱、卖萌、轻甜的题材方向
- 想把失败案例重写成更稳定的即梦 15 秒视频提示词

## 注意事项

- 技能目录名必须保持为 `feibi-jiubi-jimeng-video`
- 复制时请保留 `agents/` 与 `references/` 子目录
- 如果仓库后续新增参考文件，更新时建议整包覆盖
