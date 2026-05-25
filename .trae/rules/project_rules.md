# 项目开发规范

## 一、包管理器

**强制使用 Yarn 作为包管理器**
- 禁止使用 npm 或其他包管理器
- 所有依赖安装、更新操作必须使用 Yarn 命令

```bash
# 安装依赖
yarn install

# 添加新依赖
yarn add <package-name>

# 添加开发依赖
yarn add -D <package-name>

# 更新依赖
yarn upgrade <package-name>

# 移除依赖
yarn remove <package-name>
```

## 二、开发流程

### 1. 项目启动
```bash
# 启动开发服务器
yarn dev

# 构建生产版本
yarn build

# 预览构建结果
yarn preview
```

### 2. 代码质量保障
```bash
# 类型检查
yarn type-check

# 代码检查（自动修复）
yarn lint

# 代码格式化
yarn format
```

## 三、代码规范

### 1. TypeScript 规范
- 所有 `.vue` 文件必须使用 `<script setup lang="ts">`
- 所有函数、组件、变量必须添加类型注解
- 禁止使用 `any` 类型，除非有特殊理由

### 2. Vue 组件规范
- 优先使用 Composition API
- 组件命名使用 PascalCase
- Props 定义必须添加类型验证
- 事件命名使用 kebab-case

### 3. 代码格式化
- 必须使用 Prettier 格式化代码
- 提交代码前必须运行 `yarn format`

## 四、Git 规范

### 1. 提交信息格式
```
<类型>(<范围>): <主题>

<正文>

<页脚>
```

**类型说明**:
- feat: 新功能
- fix: 修复 bug
- docs: 文档更新
- style: 代码格式调整
- refactor: 代码重构
- test: 测试相关
- chore: 构建/工具相关

### 2. 分支策略
- `main`: 主分支，用于生产环境
- `develop`: 开发分支，用于集成功能
- `feature/*`: 功能分支，用于开发新功能
- `bugfix/*`: Bug 修复分支

## 五、环境要求

- Node.js: ^20.19.0 || >=22.12.0
- Yarn: 4.x 版本

## 六、其他规则

1. 禁止在代码中使用 `console.log`（开发环境除外）
2. 所有第三方依赖必须经过团队评审
3. 组件必须添加必要的注释和文档
4. 优先使用项目已有的工具和库，避免重复造轮子

## 七、designUI规范
- 所有UI组件必须符合designUI规范
- element-plus 组件库使用必须符合designUI规范
