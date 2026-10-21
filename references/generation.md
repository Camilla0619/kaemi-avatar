# 生成方法

## 输入与执行

生成前确认本人真实照片和所需状态齐全。先查看最少但足够的参考，传给内置 image_gen，并按实际顺序说明用途。首次从真人转换为 Q 版使用 `stylized-concept`，已有认可 Q 版图的局部修改使用 `identity-preserve`。

工具调用设置 `transparent_background: true`，除非用户要求其他背景。对可用本地图片先查看，再通过工具支持的引用方式输入；不要依赖固定本机路径。保留输出 alpha，不用不透明底色替代。仅按用户请求生成必要图片，默认不调用收费 API 或 CLI。

## 首次生成提示词骨架

```text
Use case: stylized-concept
Primary request: Create a refined, soft 3D chibi illustration of the person in the uploaded real photo, in the requested state: [状态及用户指定动作].
Input images: [按顺序注明身份、服装、动作或宠物参考].
Identity: preserve recognizable facial features, hairstyle, expression and personal characteristics from the person's photo while adapting to coherent chibi proportions.
Outfit: [本人照片的服装或用户所选服装；注明应保留的形制、颜色和细节].
Pose and props: [仅本次所需动作与道具；合理持握或穿戴].
Composition: standing full body, complete head and feet, unless another composition was requested.
Background: genuinely transparent, preserve alpha, no backdrop or baked checkerboard.
Avoid: invented personal accessories, unrelated objects, identity drift.
```

## 后续变体提示词骨架

```text
Use case: identity-preserve
Primary request: Edit the approved chibi avatar of the person in the supplied references. Change ONLY [本次变化].
Keep: exact established facial identity, chibi proportions, soft 3D finish, [未改的服装、发型、道具、构图].
Requested state: [本次状态].
Reference roles: [按实际顺序注明].
Constraints: preserve exact supplied garment details and pet markings where relevant; maintain plausible hands and object contact.
Background: genuinely transparent with alpha unless another background was requested.
```

用户的状态、服装、发型和道具分别填写，不从一个选项擅自推导其余选项。用户要求场景、半身或其他姿势时调整背景与构图行。服装文字需逐字写出并检查；宠物花色需描述具体位置，不能仅写品种或颜色。

查看成图并检查身份、服装和道具是否保持，透明背景是否实际存在；偏差只做针对性修正。图像生成无法保证每次完全一致，不把尚未检查的结果声称为已通过。
