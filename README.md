# vite-vue3-ts

[![ci](https://github.com/JS-banana/vite-vue3-ts/actions/workflows/deploy.yml/badge.svg)](https://github.com/JS-banana/vite-vue3-ts/actions/workflows/deploy.yml)

## 介绍

一个使用 `vite` + `vue3` + `pinia` + `ant-design-vue` + `typescript` 完整技术路线开发的项目，秒级开发更新启动、新的`vue3 composition api` 结合 `setup`纵享丝滑般的开发体验、全新的 `pinia`状态管理器和优秀的设计体验（`1k`的size）、`antd`无障碍过渡使用UI组件库 `ant-design-vue`、安全高效的 `typescript`类型支持、代码规范验证、多级别的权限管理~

相关文章：<https://juejin.cn/post/7041188884864040991>

## 特性

- ✨脚手架工具：高效、快速的 **Vite**
- 🔥前端框架：眼下最时髦的 **Vue3**
- 🍍状态管理器：`vue3`新秀 **Pinia**，犹如 `react zustand`般的体验，友好的api和异步处理
- 🏆开发语言：政治正确 **TypeScript**
- 🎉UI组件：`antd`开发者无障碍过渡使用 **ant-design-vue**，熟悉的配方熟悉的味道
- 🎨css样式：**less** 、`postcss`
- 📖代码规范：**Eslint**、**Prettier**、**Commitlint**
- 🔒权限管理：页面级、菜单级、按钮级、接口级
- ✊依赖按需加载：**unplugin-auto-import**，可自动导入使用到的`vue`、`vue-router`等依赖
- 💪组件按需导入：**unplugin-vue-components**，无论是第三方UI组件还是自定义组件都可实现自动按需导入以及`TS`语法提示

## 项目目录

```js
├── .husky                              // husky git hooks配置目录
    ├── _                               // husky 脚本生成的目录文件
    ├── commit-msg                      // commit-msg钩子，用于验证 message格式
    ├── pre-commit                      // pre-commit钩子，主要是和eslint配合
├── config                              // 全局配置文件
    ├── vite                            // vite 相关配置
    ├── constant.ts                     // 项目配置
    ├── themeConfig.ts                  // 主题配置
├── dist                                // 默认的 build 输出目录
├── mock                                // 前端数据mock
├── public                              // vite项目下的静态目录
└── src                                 // 源码目录
    ├── api                             // 接口相关
    ├── assets                          // 公共的文件（如image、css、font等）
    ├── components                      // 项目组件
    ├── directives                      // 自定义 指令
    ├── enums                           // 自定义 常量（枚举写法）
    ├── hooks                           // 自定义 hooks
    ├── layout                          // 全局布局
    ├── router                          // 路由
    ├── store                           // 状态管理器
    ├── utils                           // 工具库
    ├── views                           // 页面模块目录
        ├── login                       // login页面模块
        ├── ...
    ├── App.vue                         // vue顶层文件
    ├── auto-imports.d.ts               // unplugin-auto-import 插件生成
    ├── components.d.d.ts               // unplugin-vue-components 插件生成
    ├── main.ts                         // 项目入口文件
    ├── shimes-vue.d.ts                 // vite默认ts类型文件
    ├── types                           // 项目type类型定义文件夹
├── .editorconfig                       // IDE格式规范
├── .env                                // 环境变量
├── .eslintignore                       // eslint忽略
├── .eslintrc                           // eslint配置文件
├── .gitignore                          // git忽略
├── .npmrc                              // npm配置文件
├── .prettierignore                     // prettierc忽略
├── .prettierrc                         // prettierc配置文件
├── index.html                          // 入口文件
├── LICENSE.md                          // LICENSE
├── package.json                        // package
├── pnpm-lock.yaml                      // pnpm-lock
├── postcss.config.js                   // postcss
├── README.md                           // README
├── tsconfig.json                       // typescript配置文件
└── vite.config.ts                      // vite
```

## 效果图

![vite-vue3-3](https://cdn.jsdelivr.net/gh/JS-banana/images/vuepress/vite-vue3-3.jpg)

![vite-vue3-4](https://cdn.jsdelivr.net/gh/JS-banana/images/vuepress/vite-vue3-4.jpg)

## 更新记录

- 2022.01.18
  - 增加环境变量配置文件 `.env`/`.env.development`/`.env.production`
- 2022.03.09
  - 为了优化服务器构建，移除 `auto-imports.d.ts`、`components.d.ts`的git记录，加入`.gitignore`
  - 域名二级目录的路由配置优化 `history: createWebHistory(import.meta.env.BASE_URL)`
  - 路由模式由 hash调整为 history
- 2022.05.07
  - 添加路由动效`transition`，优化用户体验，并抽离封装`Breadcrumb`组件
  - 添加权限指令`v-role`，调整权限逻辑，`Table`相关组件有所改动（配合该篇文章食用[多级别权限设计思考及实战](https://ssscode.com/pages/ff7971/)）
- 2022.06.21
  - `ant-design-vue`升级到`3.x`版本
  - `dayjs`替换`moment`

## 计划

- [ ] 主题换肤功能
- [ ] 引入 `tailwindcss`
- [x] `ant-design-vue` 升级到 3.x版本

## 感谢star

[![Stargazers over time](https://starchart.cc/JS-banana/vite-vue3-ts.svg)](https://starchart.cc/JS-banana/vite-vue3-ts)
