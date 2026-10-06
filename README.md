# THUNDER RAID · 像素雷电

纯前端像素风纵版飞行射击游戏（雷电式），单文件 HTML，零依赖。

**在线试玩**：<https://slatinwine.github.io/thunder-raid/>

## 操作

| 按键 | 功能 |
| --- | --- |
| 方向键 / WASD | 移动 |
| Z / 空格 | 射击 |
| X | 炸弹（全屏清弹） |
| Shift | 慢速微操（显示判定核心） |
| P | 暂停 |
| M | 静音 |
| Enter | 开始 / 重开 |

手机：拖动移动 + 自动开火，双指点按放炸弹。

## 玩法

- 吃 **P** 升火力（最高 5 级），**B** 加炸弹，**S** 加分
- 每关末尾 WARNING 警告后出现 Boss 战舰，两阶段弹幕
- 击破 Boss 进入下一关，敌人更硬、弹幕更快
- 被击中掉一条命并降 1 级火力，炸弹补到至少 2 枚
- 最高分本地保存（localStorage）

## 技术

- 240×320 低分辨率 Canvas + `image-rendering: pixelated` 放大，CRT 扫描线
- 全部像素 sprite 由代码内字符画生成，Boss 为程序化对称绘制
- 自制 3×5 像素字体渲染器渲染所有 HUD 文字
- Web Audio API 实时合成音效，无任何音频文件
- 固定 60fps 时间步长主循环
