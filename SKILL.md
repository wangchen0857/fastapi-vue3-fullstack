---
name: fastapi-vue3-fullstack
description: 当用户说"用 fastapi-vue3-fullstack 创建一个新项目XXX"时触发，生成 FastAPI + Vue3 前后端分离的生产级项目骨架。
---

# 角色
你是一位全栈架构师，精通 FastAPI 后端与 Vue 3 前端开发。请根据用户需求生成一个前后端分离的生产级项目骨架。

# FastAPI + Vue3 全栈项目生成器

## 触发条件

当用户说"用 fastapi-vue3-fullstack 创建一个新项目XXX"时触发，其中 `XXX` 为项目名称。例如：
- "用 fastapi-vue3-fullstack 创建一个新项目 myapp"
- "用 fastapi-vue3-fullstack 创建一个新项目 demo"

## 目标

生成一个 **FastAPI 后端 + Vue3 前端** 的前后端分离生产级项目骨架。项目结构与文件内容严格按照本技能中的定义创建。

## 项目结构

以项目名 `XXX` 为例，生成的目录结构如下：

```
XXX/
├── backend/                          # FastAPI 后端
│   ├── app/
│   │   ├── __init__.py
│   │   ├── main.py                   # 应用入口，提供 / 与 /hello/{name} 路由
│   │   ├── config.py                 # 配置（空，待实现）
│   │   ├── database.py               # 数据库连接（空，待实现）
│   │   ├── dependencies.py           # 依赖注入（空，待实现）
│   │   ├── models/__init__.py        # SQLAlchemy 模型（空，待实现）
│   │   ├── routers/__init__.py       # 路由模块（空，待实现）
│   │   ├── schemas/__init__.py       # Pydantic schema（空，待实现）
│   │   └── services/__init__.py      # 业务服务（空，待实现）
│   ├── tests/
│   │   ├── __init__.py
│   │   └── test_main.http            # HTTP 测试占位文件
│   ├── requirements.txt              # Python 依赖
│   └── .env.example                  # 环境变量示例
└── frontend/                         # Vue 3 + Vite + TypeScript 前端
    ├── public/
    │   └── favicon.ico
    ├── src/
    │   ├── App.vue                   # 根组件
    │   ├── main.ts                   # 应用入口
    │   ├── assets/
    │   │   ├── base.css
    │   │   ├── main.css
    │   │   └── logo.svg
    │   ├── components/
    │   │   ├── HelloWorld.vue
    │   │   ├── TheWelcome.vue
    │   │   ├── WelcomeItem.vue
    │   │   └── icons/
    │   │       ├── IconCommunity.vue
    │   │       ├── IconDocumentation.vue
    │   │       ├── IconEcosystem.vue
    │   │       ├── IconSupport.vue
    │   │       └── IconTooling.vue
    │   ├── api/                      # API 调用层（空目录，待实现）
    │   ├── composables/              # 组合式函数（空目录，待实现）
    │   ├── layouts/                  # 布局组件（空目录，待实现）
    │   ├── router/                   # 路由配置（空目录，待实现）
    │   ├── stores/                   # 状态管理（空目录，待实现）
    │   ├── utils/                    # 工具函数（空目录，待实现）
    │   └── views/                    # 页面视图（空目录，待实现）
    ├── .vscode/
    │   └── extensions.json
    ├── .gitignore
    ├── env.d.ts
    ├── index.html
    ├── package.json
    ├── README.md
    ├── tsconfig.app.json
    ├── tsconfig.json
    ├── tsconfig.node.json
    └── vite.config.ts
```

## 生成步骤

1. 在用户指定的工作目录下创建项目根目录 `XXX/`。
2. 按照下方"文件内容"章节，逐个创建所有文件。
3. 空文件（`__init__.py`、`config.py`、`database.py`、`dependencies.py` 等）创建为空文件即可。
4. 空目录（`api/`、`composables/`、`layouts/`、`router/`、`stores/`、`utils/`、`views/`）需要创建（可放入 `.gitkeep` 占位或直接创建空目录）。
5. `public/favicon.ico` 使用标准 Vue/Vite favicon（二进制文件，可从 Vite 官方模板获取或留空）。

## 文件内容

### 根目录

#### `XXX/README.md`

```markdown
# XXX

全栈脚手架项目：FastAPI 后端 + Vue 3 + Vite + TypeScript 前端。

## 项目结构

```
XXX/
├── backend/                          # FastAPI 后端
│   ├── app/
│   │   ├── __init__.py
│   │   ├── main.py                   # 应用入口，提供 / 与 /hello/{name} 路由
│   │   ├── config.py                 # 配置（空，待实现）
│   │   ├── database.py               # 数据库连接（空，待实现）
│   │   ├── dependencies.py           # 依赖注入（空，待实现）
│   │   ├── models/__init__.py        # SQLAlchemy 模型（空，待实现）
│   │   ├── routers/__init__.py       # 路由模块（空，待实现）
│   │   ├── schemas/__init__.py       # Pydantic schema（空，待实现）
│   │   └── services/__init__.py      # 业务服务（空，待实现）
│   ├── tests/
│   │   ├── __init__.py
│   │   └── test_main.http            # HTTP 测试占位文件
│   ├── requirements.txt              # Python 依赖（含 FastAPI/Uvicorn/SQLAlchemy 等）
│   └── .env.example                  # 环境变量示例：GREETING_MESSAGE
└── frontend/                         # Vue 3 + Vite + TypeScript 前端
    ├── public/
    │   └── favicon.ico
    ├── src/
    │   ├── App.vue                   # 根组件（Vue 默认模板）
    │   ├── main.ts                   # 应用入口
    │   ├── assets/
    │   │   ├── base.css
    │   │   ├── main.css
    │   │   └── logo.svg
    │   ├── components/
    │   │   ├── HelloWorld.vue
    │   │   ├── TheWelcome.vue
    │   │   ├── WelcomeItem.vue
    │   │   └── icons/                 # 5 个预置图标组件
    │   ├── api/                      # API 调用层（空，待实现）
    │   ├── composables/              # 组合式函数（空，待实现）
    │   ├── layouts/                  # 布局组件（空，待实现）
    │   ├── router/                   # 路由配置（空，待实现）
    │   ├── stores/                   # 状态管理（空，待实现）
    │   ├── utils/                    # 工具函数（空，待实现）
    │   └── views/                    # 页面视图（空，待实现）
    ├── env.d.ts
    ├── index.html
    ├── vite.config.ts                # Vite 配置，含 `@` → `./src` 别名
    ├── tsconfig.json                 # TS 配置入口（引用 app/node 子配置）
    ├── tsconfig.app.json
    ├── tsconfig.node.json
    ├── package.json
    └── package-lock.json
```

## 技术栈

### 后端
- **框架**：FastAPI 0.115
- **运行时**：Uvicorn（ASGI）
- **数据库**：SQLAlchemy 2.0（已声明依赖，未启用）
- **校验**：Pydantic v2
- **环境变量**：python-dotenv

### 前端
- **框架**：Vue 3.5
- **构建工具**：Vite 8
- **语言**：TypeScript 6
- **类型检查**：vue-tsc
- **别名**：`@` → `./src`

## 环境要求

- **Node.js**：`^22.18.0 || >=24.12.0`
- **Python**：建议 3.10+
- **包管理器**：npm（前端）、pip（后端）

## 快速开始

### 1. 启动后端

```bash
cd backend
python -m venv .venv
source .venv/bin/activate          # Windows: .venv\Scripts\activate
pip install -r requirements.txt
cp .env.example .env               # 按需修改
uvicorn app.main:app --reload --port 8000
```

访问 http://127.0.0.1:8000 查看根路由，或访问 http://127.0.0.1:8000/docs 查看 Swagger 文档。

### 2. 启动前端

```bash
cd frontend
npm install
npm run dev
```

默认在 http://localhost:5173 启动开发服务器，支持热更新。

## 常用脚本

### 后端
| 命令 | 说明 |
| --- | --- |
| `uvicorn app.main:app --reload` | 启动开发服务器（热重载） |
| `uvicorn app.main:app` | 启动生产服务器 |
| `python -m pytest tests/` | 运行测试 |

### 前端
| 命令 | 说明 |
| --- | --- |
| `npm run dev` | 启动开发服务器 |
| `npm run build` | 类型检查 + 生产构建 |
| `npm run preview` | 预览生产构建 |
| `npm run type-check` | 仅运行类型检查 |

## API 接口

当前后端仅暴露示例接口：

| Method | Path | 描述 |
| --- | --- | --- |
| `GET` | `/` | 返回 `{"message": "Hello World"}` |
| `GET` | `/hello/{name}` | 返回 `{"message": "Hello {name}"}` |

## 当前状态

- 后端 `app/` 下 `config.py`、`database.py`、`dependencies.py` 及 `models/routers/schemas/services` 子模块为空文件 / 空目录，等待业务实现。
- 前端使用 Vue 默认模板，`api/composables/layouts/router/stores/utils/views` 等目录已建立但内容待填充。
- `tests/test_main.http` 为 HTTP 测试占位文件。

## 开发建议

- IDE：VS Code + Vue (Official) 插件（禁用 Vetur）+ Python 插件
- 前端在 `vite.config.ts` 中配置 `@` 别名指向 `src`，导入时使用 `@/...`
- 后端环境变量参考 `backend/.env.example`
- 跨域：当前前后端独立运行，对接 API 时需在 FastAPI 中配置 CORS 中间件
```

### 后端文件

#### `backend/app/__init__.py`

（空文件）

#### `backend/app/main.py`

```python
from fastapi import FastAPI

app = FastAPI()


@app.get("/")
async def root():
    return {"message": "Hello World"}


@app.get("/hello/{name}")
async def say_hello(name: str):
    return {"message": f"Hello {name}"}
```

#### `backend/app/config.py`

（空文件）

#### `backend/app/database.py`

（空文件）

#### `backend/app/dependencies.py`

（空文件）

#### `backend/app/models/__init__.py`

（空文件）

#### `backend/app/routers/__init__.py`

（空文件）

#### `backend/app/schemas/__init__.py`

（空文件）

#### `backend/app/services/__init__.py`

（空文件）

#### `backend/tests/__init__.py`

（空文件）

#### `backend/tests/test_main.http`

```http
# Test your FastAPI endpoints

GET http://127.0.0.1:8000/
Accept: application/json

###

GET http://127.0.0.1:8000/hello/User
Accept: application/json

###
```

#### `backend/requirements.txt`

```
annotated-doc==0.0.5
annotated-types==0.8.0
anyio==4.14.2
app==0.0.1
asgiref==3.10.0
bcrypt==4.2.1
blinker==1.9.0
certifi==2025.10.5
cffi==2.0.0
charset-normalizer==3.4.4
click==8.3.1
contourpy==1.3.3
cryptography==46.0.7
cycler==0.12.1
Django==5.2.7
dnspython==2.8.0
ecdsa==0.19.2
email-validator==2.3.0
fastapi==0.115.6
Flask==3.1.3
flask-cors==6.0.2
Flask-Login==0.6.3
Flask-Mail==0.10.0
Flask-SQLAlchemy==3.1.1
Flask-WTF==1.2.2
fonttools==4.60.1
h11==0.16.0
httpcore==1.0.9
httptools==0.8.0
httpx==0.28.1
idna==3.11
itsdangerous==2.2.0
Jinja2==3.1.6
kiwisolver==1.4.9
MarkupSafe==3.0.3
matplotlib==3.10.7
narwhals==2.9.0
numpy==2.3.4
packaging==25.0
pandas==2.3.3
passlib==1.7.4
pillow==12.0.0
plotly==6.3.1
pyasn1==0.6.4
pycparser==3.0
pydantic==2.10.4
pydantic-settings==2.7.0
pydantic_core==2.27.2
pygame==2.6.1
PyJWT==2.13.0
pyparsing==3.2.5
python-dateutil==2.9.0.post0
python-dotenv==1.2.2
python-http-client==3.3.7
python-jose==3.3.0
python-multipart==0.0.20
pytz==2025.2
PyYAML==6.0.3
redis==8.1.0
requests==2.32.5
rsa==4.9.1
sendgrid==6.12.5
six==1.17.0
SQLAlchemy==2.0.36
sqlparse==0.5.3
starlette==0.41.3
typing-inspection==0.4.4
typing_extensions==4.15.0
tzdata==2025.2
urllib3==2.5.0
uvicorn==0.34.0
uvloop==0.22.1
watchfiles==1.2.0
websockets==17.1
Werkzeug==3.1.7
WTForms==3.2.1
```

#### `backend/.env.example`

```
GREETING_MESSAGE=Hello, World!
```

### 前端文件

#### `frontend/package.json`

```json
{
  "name": "frontend",
  "version": "0.0.0",
  "private": true,
  "type": "module",
  "scripts": {
    "dev": "vite",
    "build": "run-p type-check \"build-only {@}\" --",
    "preview": "vite preview",
    "build-only": "vite build",
    "type-check": "vue-tsc --build"
  },
  "dependencies": {
    "vue": "^3.5.42"
  },
  "devDependencies": {
    "@tsconfig/node24": "^24.0.5",
    "@types/node": "^24.13.4",
    "@vitejs/plugin-vue": "^6.0.8",
    "@vue/tsconfig": "^0.9.1",
    "npm-run-all2": "^9.0.3",
    "typescript": "~6.0.0",
    "vite": "^8.2.2",
    "vite-plugin-vue-devtools": "^8.2.1",
    "vue-tsc": "^3.3.11"
  },
  "engines": {
    "node": "^22.18.0 || >=24.12.0"
  }
}
```

#### `frontend/vite.config.ts`

```typescript
import { fileURLToPath, URL } from 'node:url'

import { defineConfig } from 'vite'
import vue from '@vitejs/plugin-vue'
import vueDevTools from 'vite-plugin-vue-devtools'

// https://vite.dev/config/
export default defineConfig({
  plugins: [
    vue(),
    vueDevTools(),
  ],
  resolve: {
    alias: {
      '@': fileURLToPath(new URL('./src', import.meta.url)),
    },
  },
})
```

#### `frontend/index.html`

```html
<!DOCTYPE html>
<html lang="">
  <head>
    <meta charset="UTF-8">
    <link rel="icon" href="/favicon.ico">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vite App</title>
  </head>
  <body>
    <div id="app"></div>
    <script type="module" src="/src/main.ts"></script>
  </body>
</html>
```

#### `frontend/env.d.ts`

```typescript
/// <reference types="vite/client" />
```

#### `frontend/tsconfig.json`

```json
{
  "files": [],
  "references": [
    {
      "path": "./tsconfig.node.json"
    },
    {
      "path": "./tsconfig.app.json"
    }
  ]
}
```

#### `frontend/tsconfig.app.json`

```json
{
  "extends": "@vue/tsconfig/tsconfig.dom.json",
  "include": ["env.d.ts", "src/**/*", "src/**/*.vue"],
  "exclude": ["src/**/__tests__/*"],
  "compilerOptions": {
    "noUncheckedIndexedAccess": true,
    "paths": {
      "@/*": ["./src/*"]
    },
    "tsBuildInfoFile": "./node_modules/.tmp/tsconfig.app.tsbuildinfo"
  }
}
```

#### `frontend/tsconfig.node.json`

```json
{
  "extends": "@tsconfig/node24/tsconfig.json",
  "include": [
    "vite.config.*",
    "vitest.config.*",
    "cypress.config.*",
    "playwright.config.*",
    "eslint.config.*"
  ],
  "compilerOptions": {
    "module": "preserve",
    "moduleResolution": "bundler",
    "allowImportingTsExtensions": true,
    "types": ["node"],
    "noEmit": true,
    "tsBuildInfoFile": "./node_modules/.tmp/tsconfig.node.tsbuildinfo"
  }
}
```

#### `frontend/.gitignore`

```
# Logs
logs
*.log
npm-debug.log*
yarn-debug.log*
yarn-error.log*
pnpm-debug.log*
lerna-debug.log*

node_modules
.DS_Store
dist
dist-ssr
coverage
*.local

# Editor directories and files
.vscode/*
!.vscode/extensions.json
.idea
*.suo
*.ntvs*
*.njsproj
*.sln
*.sw?

*.tsbuildinfo

.eslintcache

# Cypress
/cypress/videos/
/cypress/screenshots/

# Vitest
__screenshots__/

# Vite
*.timestamp-*-*.mjs
```

#### `frontend/README.md`

```markdown
# frontend

This template should help get you started developing with Vue 3 in Vite.

## Recommended IDE Setup

[VS Code](https://code.visualstudio.com/) + [Vue (Official)](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur).

## Recommended Browser Setup

- Chromium-based browsers (Chrome, Edge, Brave, etc.):
  - [Vue.js devtools](https://chromewebstore.google.com/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd)
  - [Turn on Custom Object Formatter in Chrome DevTools](http://bit.ly/object-formatters)
- Firefox:
  - [Vue.js devtools](https://addons.mozilla.org/en-US/firefox/addon/vue-js-devtools/)
  - [Turn on Custom Object Formatter in Firefox DevTools](https://fxdx.dev/firefox-devtools-custom-object-formatters/)

## Type Support for `.vue` Imports in TS

TypeScript cannot handle type information for `.vue` imports by default, so we replace the `tsc` CLI with `vue-tsc` for type checking. In editors, we need [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) to make the TypeScript language service aware of `.vue` types.

## Customize configuration

See [Vite Configuration Reference](https://vite.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Type-Check, Compile and Minify for Production

```sh
npm run build
```
```

#### `frontend/.vscode/extensions.json`

```json
{
  "recommendations": ["Vue.volar"]
}
```

#### `frontend/src/main.ts`

```typescript
import './assets/main.css'

import { createApp } from 'vue'
import App from './App.vue'

createApp(App).mount('#app')
```

#### `frontend/src/App.vue`

```vue
<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />
    </div>
  </header>

  <main>
    <TheWelcome />
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
```

#### `frontend/src/assets/base.css`

```css
/* color palette from <https://github.com/vuejs/theme> */
:root {
  --vt-c-white: #ffffff;
  --vt-c-white-soft: #f8f8f8;
  --vt-c-white-mute: #f2f2f2;

  --vt-c-black: #181818;
  --vt-c-black-soft: #222222;
  --vt-c-black-mute: #282828;

  --vt-c-indigo: #2c3e50;

  --vt-c-divider-light-1: rgba(60, 60, 60, 0.29);
  --vt-c-divider-light-2: rgba(60, 60, 60, 0.12);
  --vt-c-divider-dark-1: rgba(84, 84, 84, 0.65);
  --vt-c-divider-dark-2: rgba(84, 84, 84, 0.48);

  --vt-c-text-light-1: var(--vt-c-indigo);
  --vt-c-text-light-2: rgba(60, 60, 60, 0.66);
  --vt-c-text-dark-1: var(--vt-c-white);
  --vt-c-text-dark-2: rgba(235, 235, 235, 0.64);
}

/* semantic color variables for this project */
:root {
  --color-background: var(--vt-c-white);
  --color-background-soft: var(--vt-c-white-soft);
  --color-background-mute: var(--vt-c-white-mute);

  --color-border: var(--vt-c-divider-light-2);
  --color-border-hover: var(--vt-c-divider-light-1);

  --color-heading: var(--vt-c-text-light-1);
  --color-text: var(--vt-c-text-light-1);

  --section-gap: 160px;
}

@media (prefers-color-scheme: dark) {
  :root {
    --color-background: var(--vt-c-black);
    --color-background-soft: var(--vt-c-black-soft);
    --color-background-mute: var(--vt-c-black-mute);

    --color-border: var(--vt-c-divider-dark-2);
    --color-border-hover: var(--vt-c-divider-dark-1);

    --color-heading: var(--vt-c-text-dark-1);
    --color-text: var(--vt-c-text-dark-2);
  }
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  font-weight: normal;
}

body {
  min-height: 100vh;
  color: var(--color-text);
  background: var(--color-background);
  transition:
    color 0.5s,
    background-color 0.5s;
  line-height: 1.6;
  font-family:
    Inter,
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    Oxygen,
    Ubuntu,
    Cantarell,
    'Fira Sans',
    'Droid Sans',
    'Helvetica Neue',
    sans-serif;
  font-size: 15px;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
```

#### `frontend/src/assets/main.css`

```css
@import './base.css';

#app {
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;
  font-weight: normal;
}

a,
.green {
  text-decoration: none;
  color: hsla(160, 100%, 37%, 1);
  transition: 0.4s;
  padding: 3px;
}

@media (hover: hover) {
  a:hover {
    background-color: hsla(160, 100%, 37%, 0.2);
  }
}

@media (min-width: 1024px) {
  body {
    display: flex;
    place-items: center;
  }

  #app {
    display: grid;
    grid-template-columns: 1fr 1fr;
    padding: 0 2rem;
  }
}
```

#### `frontend/src/assets/logo.svg`

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 261.76 226.69"><path d="M161.096.001l-30.225 52.351L100.647.001H-.005l130.877 226.688L261.749.001z" fill="#41b883"/><path d="M161.096.001l-30.225 52.351L100.647.001H52.346l78.526 136.01L209.398.001z" fill="#34495e"/></svg>
```

#### `frontend/src/components/HelloWorld.vue`

```vue
<script setup lang="ts">
defineProps<{
  msg: string
}>()
</script>

<template>
  <div class="greetings">
    <h1 class="green">{{ msg }}</h1>
    <h3>
      You've successfully created a project with
      <a href="https://vite.dev/" target="_blank" rel="noopener">Vite</a> +
      <a href="https://vuejs.org/" target="_blank" rel="noopener">Vue 3</a>.
    </h3>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
```

#### `frontend/src/components/TheWelcome.vue`

```vue
<script setup lang="ts">
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'

const openReadmeInEditor = () => fetch('/__open-in-editor?file=README.md')
</script>

<template>
  <WelcomeItem>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>Documentation</template>

    Vue's
    <a href="https://vuejs.org/" target="_blank" rel="noopener">official documentation</a>
    provides you with all information you need to get started.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <ToolingIcon />
    </template>
    <template #heading>Tooling</template>

    This project is served and bundled with
    <a href="https://vite.dev/guide/features.html" target="_blank" rel="noopener">Vite</a>. The
    recommended IDE setup is
    <a href="https://code.visualstudio.com/" target="_blank" rel="noopener">VSCode</a>
    +
    <a href="https://github.com/vuejs/language-tools" target="_blank" rel="noopener"
      >Vue - Official</a
    >. If you need to test your components and web pages, check out
    <a href="https://vitest.dev/" target="_blank" rel="noopener">Vitest</a>
    and
    <a href="https://www.cypress.io/" target="_blank" rel="noopener">Cypress</a>
    /
    <a href="https://playwright.dev/" target="_blank" rel="noopener">Playwright</a>.

    <br />

    More instructions are available in
    <a href="javascript:void(0)" @click="openReadmeInEditor"><code>README.md</code></a
    >.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <EcosystemIcon />
    </template>
    <template #heading>Ecosystem</template>

    Get official tools and libraries for your project:
    <a href="https://pinia.vuejs.org/" target="_blank" rel="noopener">Pinia</a>,
    <a href="https://router.vuejs.org/" target="_blank" rel="noopener">Vue Router</a>,
    <a href="https://test-utils.vuejs.org/" target="_blank" rel="noopener">Vue Test Utils</a>, and
    <a href="https://github.com/vuejs/devtools" target="_blank" rel="noopener">Vue Dev Tools</a>. If
    you need more resources, we suggest paying
    <a href="https://github.com/vuejs/awesome-vue" target="_blank" rel="noopener">Awesome Vue</a>
    a visit.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <CommunityIcon />
    </template>
    <template #heading>Community</template>

    Got stuck? Ask your question on
    <a href="https://chat.vuejs.org" target="_blank" rel="noopener">Vue Land</a>
    (our official Discord server), or
    <a href="https://stackoverflow.com/questions/tagged/vue.js" target="_blank" rel="noopener"
      >StackOverflow</a
    >. You should also follow the official
    <a href="https://bsky.app/profile/vuejs.org" target="_blank" rel="noopener">@vuejs.org</a>
    Bluesky account or the
    <a href="https://x.com/vuejs" target="_blank" rel="noopener">@vuejs</a>
    X account for latest news in the Vue world.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <SupportIcon />
    </template>
    <template #heading>Support Vue</template>

    As an independent project, Vue relies on community backing for its sustainability. You can help
    us by
    <a href="https://vuejs.org/sponsor/" target="_blank" rel="noopener">becoming a sponsor</a>.
  </WelcomeItem>
</template>
```

#### `frontend/src/components/WelcomeItem.vue`

```vue
<template>
  <div class="item">
    <i>
      <slot name="icon"></slot>
    </i>
    <div class="details">
      <h3>
        <slot name="heading"></slot>
      </h3>
      <slot></slot>
    </div>
  </div>
</template>

<style scoped>
.item {
  margin-top: 2rem;
  display: flex;
  position: relative;
}

.details {
  flex: 1;
  margin-left: 1rem;
}

i {
  display: flex;
  place-items: center;
  place-content: center;
  width: 32px;
  height: 32px;

  color: var(--color-text);
}

h3 {
  font-size: 1.2rem;
  font-weight: 500;
  margin-bottom: 0.4rem;
  color: var(--color-heading);
}

@media (min-width: 1024px) {
  .item {
    margin-top: 0;
    padding: 0.4rem 0 1rem calc(var(--section-gap) / 2);
  }

  i {
    top: calc(50% - 25px);
    left: -26px;
    position: absolute;
    border: 1px solid var(--color-border);
    background: var(--color-background);
    border-radius: 8px;
    width: 50px;
    height: 50px;
  }

  .item:before {
    content: ' ';
    border-left: 1px solid var(--color-border);
    position: absolute;
    left: 0;
    bottom: calc(50% + 25px);
    height: calc(50% - 25px);
  }

  .item:after {
    content: ' ';
    border-left: 1px solid var(--color-border);
    position: absolute;
    left: 0;
    top: calc(50% + 25px);
    height: calc(50% - 25px);
  }

  .item:first-of-type:before {
    display: none;
  }

  .item:last-of-type:after {
    display: none;
  }
}
</style>
```

#### `frontend/src/components/icons/IconCommunity.vue`

```vue
<template>
  <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="currentColor">
    <path
      d="M15 4a1 1 0 1 0 0 2V4zm0 11v-1a1 1 0 0 0-1 1h1zm0 4l-.707.707A1 1 0 0 0 16 19h-1zm-4-4l.707-.707A1 1 0 0 0 11 14v1zm-4.707-1.293a1 1 0 0 0-1.414 1.414l1.414-1.414zm-.707.707l-.707-.707.707.707zM9 11v-1a1 1 0 0 0-.707.293L9 11zm-4 0h1a1 1 0 0 0-1-1v1zm0 4H4a1 1 0 0 0 1.707.707L5 15zm10-9h2V4h-2v2zm2 0a1 1 0 0 1 1 1h2a3 3 0 0 0-3-3v2zm1 1v6h2V7h-2zm0 6a1 1 0 0 1-1 1v2a3 3 0 0 0 3-3h-2zm-1 1h-2v2h2v-2zm-3 1v4h2v-4h-2zm1.707 3.293l-4-4-1.414 1.414 4 4 1.414-1.414zM11 14H7v2h4v-2zm-4 0c-.276 0-.525-.111-.707-.293l-1.414 1.414C5.42 15.663 6.172 16 7 16v-2zm-.707 1.121l3.414-3.414-1.414-1.414-3.414 3.414 1.414 1.414zM9 12h4v-2H9v2zm4 0a3 3 0 0 0 3-3h-2a1 1 0 0 1-1 1v2zm3-3V3h-2v6h2zm0-6a3 3 0 0 0-3-3v2a1 1 0 0 1 1 1h2zm-3-3H3v2h10V0zM3 0a3 3 0 0 0-3 3h2a1 1 0 0 1 1-1V0zM0 3v6h2V3H0zm0 6a3 3 0 0 0 3 3v-2a1 1 0 0 1-1-1H0zm3 3h2v-2H3v2zm1-1v4h2v-4H4zm1.707 4.707l.586-.586-1.414-1.414-.586.586 1.414 1.414z"
    />
  </svg>
</template>
```

#### `frontend/src/components/icons/IconDocumentation.vue`

```vue
<template>
  <svg xmlns="http://www.w3.org/2000/svg" width="20" height="17" fill="currentColor">
    <path
      d="M11 2.253a1 1 0 1 0-2 0h2zm-2 13a1 1 0 1 0 2 0H9zm.447-12.167a1 1 0 1 0 1.107-1.666L9.447 3.086zM1 2.253L.447 1.42A1 1 0 0 0 0 2.253h1zm0 13H0a1 1 0 0 0 1.553.833L1 15.253zm8.447.833a1 1 0 1 0 1.107-1.666l-1.107 1.666zm0-14.666a1 1 0 1 0 1.107 1.666L9.447 1.42zM19 2.253h1a1 1 0 0 0-.447-.833L19 2.253zm0 13l-.553.833A1 1 0 0 0 20 15.253h-1zm-9.553-.833a1 1 0 1 0 1.107 1.666L9.447 14.42zM9 2.253v13h2v-13H9zm1.553-.833C9.203.523 7.42 0 5.5 0v2c1.572 0 2.961.431 3.947 1.086l1.107-1.666zM5.5 0C3.58 0 1.797.523.447 1.42l1.107 1.666C2.539 2.431 3.928 2 5.5 2V0zM0 2.253v13h2v-13H0zm1.553 13.833C2.539 15.431 3.928 15 5.5 15v-2c-1.92 0-3.703.523-5.053 1.42l1.107 1.666zM5.5 15c1.572 0 2.961.431 3.947 1.086l1.107-1.666C9.203 13.523 7.42 13 5.5 13v2zm5.053-11.914C11.539 2.431 12.928 2 14.5 2V0c-1.92 0-3.703.523-5.053 1.42l1.107 1.666zM14.5 2c1.573 0 2.961.431 3.947 1.086l1.107-1.666C18.203.523 16.421 0 14.5 0v2zm3.5.253v13h2v-13h-2zm1.553 12.167C18.203 13.523 16.421 13 14.5 13v2c1.573 0 2.961.431 3.947 1.086l1.107-1.666zM14.5 13c-1.92 0-3.703.523-5.053 1.42l1.107 1.666C11.539 15.431 12.928 15 14.5 15v-2z"
    />
  </svg>
</template>
```

#### `frontend/src/components/icons/IconEcosystem.vue`

```vue
<template>
  <svg xmlns="http://www.w3.org/2000/svg" width="18" height="20" fill="currentColor">
    <path
      d="M11.447 8.894a1 1 0 1 0-.894-1.789l.894 1.789zm-2.894-.789a1 1 0 1 0 .894 1.789l-.894-1.789zm0 1.789a1 1 0 1 0 .894-1.789l-.894 1.789zM7.447 7.106a1 1 0 1 0-.894 1.789l.894-1.789zM10 9a1 1 0 1 0-2 0h2zm-2 2.5a1 1 0 1 0 2 0H8zm9.447-5.606a1 1 0 1 0-.894-1.789l.894 1.789zm-2.894-.789a1 1 0 1 0 .894 1.789l-.894-1.789zm2 .789a1 1 0 1 0 .894-1.789l-.894 1.789zm-1.106-2.789a1 1 0 1 0-.894 1.789l.894-1.789zM18 5a1 1 0 1 0-2 0h2zm-2 2.5a1 1 0 1 0 2 0h-2zm-5.447-4.606a1 1 0 1 0 .894-1.789l-.894 1.789zM9 1l.447-.894a1 1 0 0 0-.894 0L9 1zm-2.447.106a1 1 0 1 0 .894 1.789l-.894-1.789zm-6 3a1 1 0 1 0 .894 1.789L.553 4.106zm2.894.789a1 1 0 1 0-.894-1.789l.894 1.789zm-2-.789a1 1 0 1 0-.894 1.789l.894-1.789zm1.106 2.789a1 1 0 1 0 .894-1.789l-.894 1.789zM2 5a1 1 0 1 0-2 0h2zM0 7.5a1 1 0 1 0 2 0H0zm8.553 12.394a1 1 0 1 0 .894-1.789l-.894 1.789zm-1.106-2.789a1 1 0 1 0-.894 1.789l.894-1.789zm1.106 1a1 1 0 1 0 .894 1.789l-.894-1.789zm2.894.789a1 1 0 1 0-.894-1.789l.894 1.789zM8 19a1 1 0 1 0 2 0H8zm2-2.5a1 1 0 1 0-2 0h2zm-7.447.394a1 1 0 1 0 .894-1.789l-.894 1.789zM1 15H0a1 1 0 0 0 .553.894L1 15zm1-2.5a1 1 0 1 0-2 0h2zm12.553 2.606a1 1 0 1 0 .894 1.789l-.894-1.789zM17 15l.447.894A1 1 0 0 0 18 15h-1zm1-2.5a1 1 0 1 0-2 0h2zm-7.447-5.394l-2 1 .894 1.789 2-1-.894-1.789zm-1.106 1l-2-1-.894 1.789 2 1 .894-1.789zM8 9v2.5h2V9H8zm8.553-4.894l-2 1 .894 1.789 2-1-.894-1.789zm.894 0l-2-1-.894 1.789 2 1 .894-1.789zM16 5v2.5h2V5h-2zm-4.553-3.894l-2-1-.894 1.789 2 1 .894-1.789zm-2.894-1l-2 1 .894 1.789 2-1L8.553.106zM1.447 5.894l2-1-.894-1.789-2 1 .894 1.789zm-.894 0l2 1 .894-1.789-2-1-.894 1.789zM0 5v2.5h2V5H0zm9.447 13.106l-2-1-.894 1.789 2 1 .894-1.789zm0 1.789l2-1-.894-1.789-2 1 .894 1.789zM10 19v-2.5H8V19h2zm-6.553-3.894l-2-1-.894 1.789 2 1 .894-1.789zM2 15v-2.5H0V15h2zm13.447 1.894l2-1-.894-1.789-2 1 .894 1.789zM18 15v-2.5h-2V15h2z"
    />
  </svg>
</template>
```

#### `frontend/src/components/icons/IconSupport.vue`

```vue
<template>
  <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="currentColor">
    <path
      d="M10 3.22l-.61-.6a5.5 5.5 0 0 0-7.666.105 5.5 5.5 0 0 0-.114 7.665L10 18.78l8.39-8.4a5.5 5.5 0 0 0-.114-7.665 5.5 5.5 0 0 0-7.666-.105l-.61.61z"
    />
  </svg>
</template>
```

#### `frontend/src/components/icons/IconTooling.vue`

```vue
<!-- This icon is from <https://github.com/Templarian/MaterialDesign>, distributed under Apache 2.0 (https://www.apache.org/licenses/LICENSE-2.0) license-->
<template>
  <svg
    xmlns="http://www.w3.org/2000/svg"
    xmlns:xlink="http://www.w3.org/1999/xlink"
    aria-hidden="true"
    role="img"
    class="iconify iconify--mdi"
    width="24"
    height="24"
    preserveAspectRatio="xMidYMid meet"
    viewBox="0 0 24 24"
  >
    <path
      d="M20 18v-4h-3v1h-2v-1H9v1H7v-1H4v4h16M6.33 8l-1.74 4H7v-1h2v1h6v-1h2v1h2.41l-1.74-4H6.33M9 5v1h6V5H9m12.84 7.61c.1.22.16.48.16.8V18c0 .53-.21 1-.6 1.41c-.4.4-.85.59-1.4.59H4c-.55 0-1-.19-1.4-.59C2.21 19 2 18.53 2 18v-4.59c0-.32.06-.58.16-.8L4.5 7.22C4.84 6.41 5.45 6 6.33 6H7V5c0-.55.18-1 .57-1.41C7.96 3.2 8.44 3 9 3h6c.56 0 1.04.2 1.43.59c.39.41.57.86.57 1.41v1h.67c.88 0 1.49.41 1.83 1.22l2.34 5.39z"
      fill="currentColor"
    ></path>
  </svg>
</template>
```

### 空目录

以下目录创建为空目录即可（可放入 `.gitkeep` 文件占位以保留空目录）：

- `frontend/src/api/`
- `frontend/src/composables/`
- `frontend/src/layouts/`
- `frontend/src/router/`
- `frontend/src/stores/`
- `frontend/src/utils/`
- `frontend/src/views/`

### 二进制文件

`frontend/public/favicon.ico` 为二进制图标文件，使用标准 Vue/Vite favicon 即可。可从 Vite 官方模板获取，或留空使用浏览器默认图标。

## 注意事项

1. `requirements.txt` 为完整依赖锁定列表，包含 FastAPI、Uvicorn、SQLAlchemy、Pydantic v2 等核心依赖。如需精简，可仅保留 FastAPI 相关依赖。
2. 空文件（`__init__.py`、`config.py` 等）保持为空，等待业务实现。
3. 前端 `@` 别名已在 `vite.config.ts` 和 `tsconfig.app.json` 中配置指向 `./src`。
4. 后端启动后可通过 `http://127.0.0.1:8000/docs` 访问 Swagger 自动文档。
5. 前后端独立运行，对接 API 时需在 FastAPI 中配置 CORS 中间件。
