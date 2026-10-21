# Kaemi Avatar

根据你上传的本人真实照片和指定状态，生成精致柔和的 3D Q 版个人形象。支持 casual、work、training 及自定义状态，后续可独立改变服装、发型、动作和道具。

此公开包不包含任何个人照片、专属人物或宠物预设。

## 安装

将本目录放到 Codex 的 skills 目录，使文件结构为 `~/.codex/skills/kaemi-avatar/SKILL.md`。如果配置了 `CODEX_HOME`，则使用其下的 `skills/kaemi-avatar`。重新打开会话后调用。

## 使用

先上传本人的真实照片，再发送：

> 请用 $kaemi-avatar，根据我上传的照片制作 casual 状态的 Q 版形象，透明背景、站立全身。

也可以指定工作动作、运动服参考、发型或道具。需要加入自己的宠物时，一并上传宠物参考图。缺少本人照片或状态时，skill 会先提醒补充。

## 环境

需要支持技能和内置 image_gen 的 Codex 环境；可配合 imagegen skill 使用。默认透明 PNG 风格输出，属于静态图片，不是真实 3D 模型或 ChatGPT Work Pet。图片生成可能消耗所在环境的额度，技能本身不自动生成全套变体。

私人参考和生成结果应留在使用者自己的工作区，不要提交到本公开包。
