# 途序 Tripwise｜旅行规划与行中调整原型

**[直接体验交互原型](https://yyyyskbfxx.github.io/Tripwise/)** · [作品集案例说明](https://yyyyskbfxx.github.io/AI-Demo/travel-project.html)

途序面向旅行前收藏了很多地点、却难以排出合适路线的自由行用户。它把“选择真正想去的地方”和“旅途中发生变化后如何调整”放进同一条流程：先表达地点优先级与旅行偏好，再生成可调整的日程；遇到变化时比较 Plan B 的影响，由用户决定是否应用。

## 界面展示

| 首页与地点选择 | 旅行偏好与路线方案 |
| --- | --- |
| [![途序首页：当前旅程与规划入口](images/tripwise/previews/home.png)](images/tripwise/home.png) [![地点选择：标注必去、想去和顺路](images/tripwise/previews/places.png)](images/tripwise/places.png) | [![偏好设置：天数、节奏、主题和交通](images/tripwise/previews/preferences.png)](images/tripwise/preferences.png) [![路线方案：按天查看地点与时间](images/tripwise/previews/route.png)](images/tripwise/route.png) |

| 行中进度与变化 | Plan B 对比 |
| --- | --- |
| [![行中助手：查看当前路线与进度](images/tripwise/previews/journey.png)](images/tripwise/journey.png) [![变化处理：延长停留时间后的调整入口](images/tripwise/previews/delay.png)](images/tripwise/delay.png) | [![Plan B：比较顺延、替换与减少一站](images/tripwise/previews/planb.png)](images/tripwise/planb.png) |

点击缩略图可查看完整界面。上述截图与在线原型使用演示地点和情境。

## 产品背景与目标用户

旅行规划常从不同平台的收藏开始。用户需要自行判断哪些地点必须保留、哪些可以顺路加入，再考虑天数、节奏、主题和交通方式。行中遇到停留延长、天气或人流变化时，原路线还需要重新权衡。途序的目标用户是希望保留自主选择、同时减少反复排程成本的自由行用户。

## 产品目标与设计判断

1. **先表达优先级，再排路线。** “必去、想去、顺路”比一个无差别收藏列表更能反映取舍。
2. **把偏好变成可见条件。** 天数、出发时间、节奏、主题和交通方式会参与前端排程，用户能看到它们怎样影响结果。
3. **变化后展示代价。** Plan B 提供保留顺延、相近替换和减少一站等候选方案，比较对原计划的影响；任何调整都需用户确认。

## 核心流程

首页进入规划 → 选择城市和地点并标注优先级 → 设置偏好 → 查看按天排布的路线 → 进入行中助手 → 触发模拟变化 → 比较并确认 Plan B。当前页面会话保留路线历史，刷新后重置。

## 实现与范围

原型使用原生 HTML、CSS、JavaScript。`travel.js` 包含地点数据、偏好权重、路线生成和候选调整逻辑；`travel.css` 负责响应式界面；`images/tripwise/` 是界面截图。打开 `index.html` 即可本地体验。

当前是规则驱动的交互演示。地点位置、路程、时间、天气、人流和交通变化为模拟或估算数据；尚未接入实时地图、交通或天气服务，路线也未经过真实出行验证。

SEO GEO做好
