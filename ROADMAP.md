# ROADMAP

> 工作档案路线图。当前目标：把招聘官网（qtrecurit Site）展示的公开信息同步一份到本仓库，使 profile 成为面向求职者的公开人力资源档案。

## 定位与同步方向

qtrecurit Site（`apps/qtrecurit/src/site`）是对外招聘门户，直接服务投递流程；本仓库是公开工作档案，承载同一批信息的存档视图。两者分工：

- 招聘官网是事实源，负责运营与更新；
- 本仓库单向同步官网已公开的信息，不做独立撰写，不承载未公开的内部信息。

## 同步范围

官网当前公开的信息共五类：

- 公司简介与主营业务（Home 页）；
- 实习岗位与报名方式（Intern 页，岗位数据来自 `src/data/positions.ts`）；
- 考核方式（Intern 页摘要与 Assessment 页完整版）；
- 兼职岗位、提成与结算、兼职流程（Parttime 页）；
- 简历要求与求职信要求（Application 页）。

## 版本规划

- 同步文档按主题分为 `plan/` 与 `recruitment/` 两个目录：`plan/` 侧重岗位编制（`intern.md` 实习岗位、`parttime.md` 兼职岗位与提成结算），`recruitment/` 侧重招聘考核（`application.md` 报名方式与简历、求职信要求，`assessment.md` 考核方式）；
- 公司简介与主营业务并入 `index.md`，并登记新增文档；
- 每份文档头部标注来源文件路径，保证可回溯到官网对应页面；
- 更新 CHANGELOG 并在父仓库更新子模块引用。
