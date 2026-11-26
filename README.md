# 判断一个岗位 · Portfolio

把「这个岗位值不值得投」做成一套**可被反驳**的判断流程：从一份招聘 JD 出发，逆向还原公司的真实业务、岗位的实际工作内容、招聘方会让步的条件，以及这段经历对候选人 3–5 年的方向影响。

单页静态站点，零依赖，纯 HTML / CSS / 原生 JS。

## 在线预览

已通过 GitHub Actions 发布到 GitHub Pages：

```
https://ershuai-acc.github.io/case-jd/
```

## 本地预览

```bash
python3 -m http.server 8811
# 打开 http://127.0.0.1:8811
```

或直接双击 `index.html`（无需构建）。

## 页面结构

| 章节 | 内容 |
|---|---|
| Hero | 主张：判断应当可被反驳 |
| 01 起点 | 岗位分析的三种失真：愿望清单≠筛选清单、职责≠日常、薪资≠定位 |
| 02 方法 | 六个动作：事实层 → 公司尽调 → 实况还原 → 矛盾检验 → 稀缺性定价 → 价值推演 |
| 03 机制 | 稀缺性定价：越不可培养越不让步，越可学越容易让步 |
| 04 案例 | 一次检索改写整份判断（惟景三维 · 高级软件产品经理） |
| 05 纪律 | 证据分级 A/B/C/D、未核实项、"我可能错了"的信号 |
| 06 视角 | 作为猎头 / 作为 AI 学习者 |

## 自动部署

`.github/workflows/pages.yml` 在每次 push 到 `main` 时触发：

1. `actions/configure-pages` —— 若 Pages 尚未开启则自动开启（`enablement: true`）
2. `actions/upload-pages-artifact` —— 打包仓库根目录
3. `actions/deploy-pages` —— 发布到 Pages

首次运行需要仓库允许 Actions 写入 Pages（`pages: write` + `id-token: write`，已在 workflow 中声明）。

## 说明

- 页面中的候选人简历为**模拟样本**，用于演示评估流程，非真实个人信息。
- 案例中的公司信息来自公开渠道（官网、工商、媒体报道），结论属于方法论演示，不构成对任何企业的评价或投资、求职建议。
- 联系方式为占位符，请替换后再公开分享。

## License

内容与代码仅用于作品展示，转载请联系作者。
