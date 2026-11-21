# 04 · 课堂交互作品三则

## 所属
- 对话：DSH 会话 2026-11-21（课堂交互作业）
- 主题：情境沉浸式 / 探究操作式 / 创作生成式 三类课堂交互作品，选做三项，配教学目的说明

## 在线地址（作品集首页）
https://xxxxy-tech.github.io/teaching-interactions/

| 序号 | 作品 | 交互类型 | 学科 | 在线链接 |
|---|---|---|---|---|
| 01 | 背影 · 浦口车站 | 情境沉浸式 | 语文（统编版八上 第 14 课） | https://xxxxy-tech.github.io/teaching-interactions/01-beiying-station/ |
| 02 | 勾股定理探究实验室 | 探究操作式 | 数学（北师大版八上 第一章） | https://xxxxy-tech.github.io/teaching-interactions/02-pythagoras-lab/ |
| 03 | 意象诗坊 | 创作生成式 | 语文（统编版八上 第三单元后） | https://xxxxy-tech.github.io/teaching-interactions/03-imagery-studio/ |

## 产物清单
- `index.html` —— 作品集首页（三张入口卡片，说明三类交互形态）
- `01-beiying-station/index.html` —— 第一人称进入 1917 年浦口车站，四个慢镜头逐个辨析「攀、缩、倾、爬」，通关后打开「四次背影 / 四次流泪」时间轴
- `02-pythagoras-lab/index.html` —— 拖动直角边改变 a、b，三个正方形面积联动；记录≥3 组数据后解锁猜想，答对后逐层展开赵爽弦图面积证明
- `03-imagery-studio/index.html` —— 挑意象 → 系统按平仄与押韵拼出五言绝句毛坯 → 逐词替换、实时算合律度 → 导出竖排诗笺 SVG
- `教学目的说明.docx` —— 三条教学目的、课堂使用建议、在线链接（可点击）
- `.gitignore` —— 排除下划线开头的临时截图与测试文件

四个 HTML 全部自包含：无外部 JS/CSS/字体/图片依赖，断网也能用，双击即可打开。

## 技术要点
- 全部为单文件原生 HTML + CSS + 内联 SVG + 原生 JS，无构建步骤、无框架
- 02 的视图按内容边界动态计算 viewBox，图形随 a、b 变化始终居中；弦图在 |a−b| 过小时按 3:4 示意并加注说明
- 03 的平仄判定按普通话四声简化（一二声为平、三四声为仄），未计古入声，教学说明中已注明是示意

## 当前进度
- [x] 三个作品开发完成并逐条交互验证（Edge headless 注入脚本跑通全流程）
- [x] 作品集首页
- [x] 发布到 GitHub Pages，四个地址均返回 200
- [x] 教学目的说明 Word（6 页，含三张作品配图、可点击链接、课堂使用建议、设计说明）
- [x] 清理临时文件

## 说明
- 仓库：https://github.com/xxxxy-tech/teaching-interactions（公开）
- Pages 发布方式：仓库根目录（main 分支 /），提交后约 1 分钟生效
- 本机 git 直连 github.com 推送会超时，文件通过 gh api（Contents API）上传，勿直接 git push
