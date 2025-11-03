# @harmory_study/basic

这是一个关于minder使用的鸿蒙开发学习的工具包，提供基础工具类和组件。

## 安装

使用ohpm安装：

```bash
ohpm install @harmory_study/basic
# 或
ohpm i @harmory_study/basic
```

## 使用说明

### 导入模块

```typescript
import { RouterMap, RouterModule, Logger, PreferenceUtil } from '@harmory_study/basic';
```

### 主要功能

#### 1. 路由管理 (RouterModule)
- 提供页面跳转、参数传递、返回等路由功能
- 支持push、replace、pop等操作

```typescript
// 页面跳转
RouterModule.push(RouterMap.HOME_PAGE, { id: 1 });

// 获取参数
const params = RouterModule.getNavParam<MyParams>(RouterMap.MY_PAGE);
```

#### 2. 日志工具 (Logger)
- 提供统一的日志输出功能
- 支持info、error、warn等级别

```typescript
Logger.info('TAG', '日志信息');
Logger.error('TAG', '错误信息');
```

#### 3. 偏好设置 (PreferenceUtil)
- 提供本地存储功能
- 支持字符串、数字、布尔值等数据类型

```typescript
const prefs = PreferenceUtil.getInstance();
prefs.put('key', 'value');
const value = prefs.get('key', 'default');
```

#### 4. 路由映射 (RouterMap)
- 定义所有页面的路由名称
- 统一管理页面跳转路径

```typescript
export enum RouterMap {
  HOME_PAGE = 'HomePage',
  COURSE_DETAIL_PAGE = 'CourseDetailPage',
  MESSAGE_PAGE = 'MessagePage'
}
```

### 依赖关系

- HarmonyOS SDK >= 5.0.0
- 无其他三方库依赖

### 文件结构

```
basic/
├── src/main/ets/
│   ├── components/     # 公共组件
│   ├── constants/      # 常量定义
│   ├── types/          # 类型定义
│   └── utils/          # 工具类
├── Index.ets           # 入口文件
└── README.md          # 说明文档
```

### 版本信息

- 当前版本：1.0.0
- 支持HarmonyOS：>= 5.0.0

### 问题反馈

如有问题请提交到 [GitHub Issues](https://github.com/minderers/basic.git/issues)