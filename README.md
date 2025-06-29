# 食光机 - 智能食材管理小程序

## 项目介绍
食光机是一款基于微信小程序平台的智能食材管理应用，旨在帮助用户更好地管理厨房食材，减少食物浪费，提供健康饮食建议。通过AI智能识别、过期提醒、营养分析、膳食计划等功能，为用户提供全方位的食材管理解决方案。

## 项目结构

```
食光机-cursor/
├── app.js                          # 小程序入口文件，全局配置和登录状态管理
├── app.json                        # 全局配置文件，页面路由和tabBar配置
├── app.wxss                        # 全局样式文件
├── sitemap.json                    # 站点地图配置
├── project.config.json             # 项目配置文件
├── project.private.config.json     # 项目私有配置文件（包含个人设置）
├── .eslintrc.js                    # ESLint代码规范配置
├── .gitignore                      # Git忽略文件配置
├── README.md                       # 项目说明文档
│
├── assets/                         # 静态资源目录
│   ├── icons/                      # 图标文件
│   │   ├── about.svg               # 关于图标
│   │   ├── agreement.svg           # 协议图标
│   │   ├── arrow-right.svg         # 右箭头图标
│   │   ├── calorie.svg             # 热量图标
│   │   ├── calories.svg            # 卡路里图标
│   │   ├── camera.svg              # 相机图标
│   │   ├── capture.svg             # 拍摄图标
│   │   ├── check.svg               # 检查图标
│   │   ├── child-avatar.svg        # 儿童头像图标
│   │   ├── close.svg               # 关闭图标
│   │   ├── consultant.svg          # 咨询师图标
│   │   ├── elderly-avatar.svg      # 老人头像图标
│   │   ├── email.svg               # 邮箱图标
│   │   ├── expiring.svg            # 临期图标
│   │   ├── family.svg              # 家庭图标
│   │   ├── fitness-avatar.svg      # 健身头像图标
│   │   ├── fresh.svg               # 新鲜图标
│   │   ├── fun_fact.svg            # 趣味知识图标
│   │   ├── gallery.svg             # 相册图标
│   │   ├── health_note.svg         # 健康提示图标
│   │   ├── help.svg                # 帮助图标
│   │   ├── myself-avatar.svg       # 个人头像图标
│   │   ├── notification.svg        # 通知图标
│   │   ├── nutrition.svg           # 营养图标
│   │   ├── phone.svg               # 电话图标
│   │   ├── points.svg              # 积分图标
│   │   ├── pregnant-avatar.svg     # 孕妇头像图标
│   │   ├── privacy.svg             # 隐私图标
│   │   ├── refresh.svg             # 刷新图标
│   │   ├── reminder.svg            # 提醒图标
│   │   ├── restriction.svg         # 限制图标
│   │   ├── swipe.svg               # 滑动图标
│   │   ├── time.svg                # 时间图标
│   │   ├── tip.svg                 # 小贴士图标
│   │   ├── vip.svg                 # VIP图标
│   │   ├── warning.svg             # 警告图标
│   │   ├── website.svg             # 网站图标
│   │   └── wechat.svg              # 微信图标
│   ├── images/                     # 图片文件
│   │   └── logo.svg                # 应用Logo
│   └── tabbar/                     # 底部导航栏图标
│       ├── home.png                # 首页图标（未选中）
│       ├── home_selected.png       # 首页图标（选中）
│       ├── scan.png                # 扫描图标（未选中）
│       ├── scan_selected.png       # 扫描图标（选中）
│       ├── plan.png                # 计划图标（未选中）
│       ├── plan_selected.png       # 计划图标（选中）
│       ├── nutrition.png           # 营养图标（未选中）
│       ├── nutrition_selected.png  # 营养图标（选中）
│       ├── profile.png             # 个人图标（未选中）
│       └── profile_selected.png    # 个人图标（选中）
│
├── components/                     # 自定义组件目录
│   ├── ec-canvas/                  # ECharts图表组件
│   │   ├── ec-canvas.js            # 组件逻辑文件
│   │   ├── ec-canvas.json          # 组件配置文件
│   │   ├── ec-canvas.wxml          # 组件模板文件
│   │   ├── ec-canvas.wxss          # 组件样式文件
│   │   ├── echarts.js              # ECharts核心库
│   │   └── wx-canvas.js            # 微信Canvas适配器
│   └── section-header/             # 页面标题组件
│       ├── section-header.js       # 组件逻辑文件
│       ├── section-header.json     # 组件配置文件
│       ├── section-header.wxml     # 组件模板文件
│       └── section-header.wxss     # 组件样式文件
│
├── pages/                          # 页面目录
│   ├── index/                      # 首页
│   │   ├── index.js                # 页面逻辑
│   │   ├── index.json              # 页面配置
│   │   ├── index.wxml              # 页面结构
│   │   └── index.wxss              # 页面样式
│   ├── login/                      # 登录页
│   │   ├── login.js
│   │   ├── login.json
│   │   ├── login.wxml
│   │   └── login.wxss
│   ├── scan/                       # 扫描识别页
│   │   ├── scan.js
│   │   ├── scan.json
│   │   ├── scan.wxml
│   │   └── scan.wxss
│   ├── plan/                       # 膳食计划页
│   │   ├── plan.js
│   │   ├── plan.json
│   │   ├── plan.wxml
│   │   └── plan.wxss
│   ├── nutrition/                  # 营养分析页
│   │   ├── nutrition.js
│   │   ├── nutrition.json
│   │   ├── nutrition.wxml
│   │   └── nutrition.wxss
│   ├── profile/                    # 个人中心页
│   │   ├── profile.js
│   │   ├── profile.json
│   │   ├── profile.wxml
│   │   └── profile.wxss
│   ├── inventory/                  # 库存管理页
│   │   ├── inventory.js
│   │   ├── inventory.json
│   │   ├── inventory.wxml
│   │   └── inventory.wxss
│   ├── recipe-detail/              # 菜谱详情页
│   │   ├── recipe-detail.js
│   │   ├── recipe-detail.json
│   │   ├── recipe-detail.wxml
│   │   └── recipe-detail.wxss
│   ├── expiring-recipes/           # 临期急救站页
│   │   ├── expiring-recipes.js
│   │   ├── expiring-recipes.json
│   │   ├── expiring-recipes.wxml
│   │   └── expiring-recipes.wxss
│   ├── family/                     # 家庭管理页
│   │   ├── family.js
│   │   ├── family.json
│   │   ├── family.wxml
│   │   └── family.wxss
│   ├── restrictions/               # 饮食禁忌页
│   │   ├── restrictions.js
│   │   ├── restrictions.json
│   │   ├── restrictions.wxml
│   │   └── restrictions.wxss
│   ├── settings/                   # 设置页面目录
│   │   ├── calorie-target/         # 热量目标设置
│   │   │   ├── calorie-target.js
│   │   │   ├── calorie-target.json
│   │   │   ├── calorie-target.wxml
│   │   │   └── calorie-target.wxss
│   │   ├── nutrition-elements-target/  # 营养元素目标设置
│   │   │   ├── nutrition-elements-target.js
│   │   │   ├── nutrition-elements-target.json
│   │   │   ├── nutrition-elements-target.wxml
│   │   │   └── nutrition-elements-target.wxss
│   │   └── push-preferences/       # 推送偏好设置
│   │       ├── push-preferences.js
│   │       ├── push-preferences.json
│   │       ├── push-preferences.wxml
│   │       └── push-preferences.wxss
│   ├── legal/                      # 法律条款页面目录
│   │   ├── privacy-policy/         # 隐私政策
│   │   │   ├── privacy-policy.js
│   │   │   ├── privacy-policy.json
│   │   │   ├── privacy-policy.wxml
│   │   │   └── privacy-policy.wxss
│   │   └── user-agreement/         # 用户协议
│   │       ├── user-agreement.js
│   │       ├── user-agreement.json
│   │       ├── user-agreement.wxml
│   │       └── user-agreement.wxss
│   ├── help/                       # 帮助页
│   │   ├── help.js
│   │   ├── help.json
│   │   ├── help.wxml
│   │   └── help.wxss
│   └── about/                      # 关于页
│       ├── about.js
│       ├── about.json
│       ├── about.wxml
│       └── about.wxss
│
├── utils/                          # 工具类目录
│   ├── api.js                      # API请求封装和数据处理
│   └── router.js                   # 路由管理和权限控制
│
└── docs/                           # 项目文档目录
    ├── 前端页面设计文档.md          # 前端设计规范文档
    └── 开发任务清单.md              # 开发进度和任务管理
```

## 技术架构

### 前端技术栈
- **开发框架**: 微信小程序原生开发框架
- **UI组件**: 原生小程序组件 + 自定义组件
- **数据可视化**: ECharts 图表库
- **样式架构**: WXSS + 响应式设计(rpx单位)
- **组件化**: 模块化组件开发，提高代码复用性

### 后端技术栈
- **API架构**: RESTful API
- **数据格式**: JSON
- **图像识别**: AI食材识别服务
- **用户认证**: JWT Token认证
- **数据存储**: 云端存储 + 本地缓存

### 开发环境
- **开发工具**: 微信开发者工具
- **基础库版本**: 3.0.0+
- **兼容性**: 支持iOS和Android微信客户端
- **代码规范**: ESLint代码检查

## 核心功能特性

### 🔍 智能食材识别
- **AI图像识别**: 支持拍照或相册选择，自动识别食材种类
- **多维度信息**: 自动识别食材名称、建议数量、存储天数
- **丰富信息展示**: 
  - 置信度评分显示识别准确性
  - 趣味知识(fun_fact)增加用户兴趣
  - 健康提示(health_note)提供营养建议
  - 烹饪小贴士(tip)指导食材使用
- **智能数据处理**: 
  - 支持多种计量单位(个、克、千克、根、颗、袋、瓶、盒等)
  - 自动计算过期日期
  - 一键保存至库存系统
- **即时菜谱推荐**: 基于识别食材智能推荐匹配菜谱

### 📦 智能库存管理
- **分类管理**: 自动分类为新鲜食材、临期食材、过期食材
- **实时统计**: 动态显示各类食材数量统计
- **过期预警**: 智能计算剩余保质期，提供分级预警
- **便捷操作**: 
  - 支持食材信息编辑(数量、过期日期)
  - 一键删除过期食材
  - 批量管理功能
- **数据同步**: 实时从后端获取最新库存数据

### 🍳 智能菜谱推荐系统
- **多源推荐**: 
  - 基于库存食材的智能匹配
  - 临期食材优先推荐
  - 个性化推荐算法
- **详细信息展示**: 
  - 菜谱匹配度评分
  - 制作时间和难度
  - 热量和营养信息
- **菜谱详情页**: 
  - 分步骤烹饪指导
  - 食材清单(主料、辅料、调料分类)
  - 工具准备和替代方案
  - 预处理指南
  - 专业烹饪技巧和小贴士

### 📊 营养分析与可视化
- **多维度图表**: 
  - 环形图展示三大营养素比例(蛋白质、脂肪、碳水化合物)
  - 折线图对比每日热量摄入与目标值
  - 雷达图分析维生素和矿物质达标率
- **时间维度分析**: 支持今日、本周、本月营养数据查看
- **营养素详情**: 
  - 进度条直观显示各营养素达标情况
  - 食物来源分析(如"钙摄入65%来自牛奶")
  - 个性化营养建议
- **交互式体验**: 点击图表可查看详细数据和建议

### 📅 膳食计划管理
- **周计划视图**: 
  - 日历式界面展示一周三餐安排
  - 支持日期选择和快速切换
  - 营养汇总和目标对比
- **智能推荐**: 
  - 基于库存食材生成餐饮建议
  - 营养均衡性分析
  - 临期食材优先使用
- **批量操作**: 
  - 一键生成购物清单
  - 分享食谱计划
  - 营养目标达标提醒

### 👥 家庭多成员管理
- **成员档案**: 
  - 预设成员类型(成人、儿童、孕妇、老人、健身人士)
  - 个性化营养目标设置
  - 独立的饮食禁忌管理
- **智能适配**: 
  - 根据成员特点调整推荐菜谱
  - 营养需求冲突检测
  - 一键切换成员视图

### 🚫 饮食禁忌管理
- **全面覆盖**: 
  - 过敏源管理(贝类、乳制品、坚果、鸡蛋等)
  - 宗教饮食禁忌(不吃猪肉、牛肉、全素食等)
  - 自定义禁忌添加
- **智能过滤**: 根据禁忌自动过滤不适合的菜谱
- **家庭适配**: 为不同家庭成员设置独立禁忌

### ⚡ 临期急救站
- **紧急度分级**: 
  - 红色(1天内过期)
  - 橙色(3天内过期) 
  - 黄色(5天内过期)
- **创意菜谱**: 专门针对临期食材的创意搭配
- **匹配评分**: 显示食材与菜谱的匹配程度
- **减少浪费**: 智能建议帮助用户充分利用临期食材

### 👤 个人中心与设置
- **用户档案**: 
  - 个人信息管理(头像、昵称、健康目标)
  - 会员等级和积分系统
  - 营养师咨询服务
- **个性化设置**: 
  - 热量目标设置(减脂、维持、增肌模式)
  - 营养元素目标精细化调整
  - 保质期提醒时间自定义
- **隐私安全**: 
  - 推送偏好设置
  - 免打扰时间设置
  - 数据权限管理

## 页面结构与导航

### 主要页面
- **首页** (`/pages/index/index`): 今日推荐菜谱、食材库存概览、快捷功能入口
- **识别页** (`/pages/scan/scan`): 拍照识别食材、编辑食材信息、即时菜谱推荐
- **计划页** (`/pages/plan/plan`): 周餐饮计划、营养目标管理、购物清单生成
- **营养页** (`/pages/nutrition/nutrition`): 营养数据可视化、健康分析报告
- **我的页** (`/pages/profile/profile`): 个人信息、设置中心、会员服务

### 功能页面
- **库存管理** (`/pages/inventory/inventory`): 食材库存分类管理
- **菜谱详情** (`/pages/recipe-detail/recipe-detail`): 详细烹饪指导
- **临期急救站** (`/pages/expiring-recipes/expiring-recipes`): 临期食材菜谱推荐
- **家庭管理** (`/pages/family/family`): 多成员档案管理
- **饮食禁忌** (`/pages/restrictions/restrictions`): 过敏源和禁忌管理

### 设置页面
- **热量目标** (`/pages/settings/calorie-target/calorie-target`): 每日热量目标设置
- **营养目标** (`/pages/settings/nutrition-elements-target/nutrition-elements-target`): 营养素目标设置
- **推送设置** (`/pages/settings/push-preferences/push-preferences`): 通知偏好管理

### 辅助页面
- **帮助中心** (`/pages/help/help`): 使用指南和常见问题
- **关于我们** (`/pages/about/about`): 应用信息和版本说明
- **隐私政策** (`/pages/legal/privacy-policy/privacy-policy`): 隐私条款
- **用户协议** (`/pages/legal/user-agreement/user-agreement`): 服务条款

## 核心组件与工具

### 自定义组件
- **section-header**: 全局页面标题组件，支持居中、左对齐、右对齐
- **ec-canvas**: ECharts图表组件，支持多种数据可视化图表

### 工具模块
- **api.js**: 统一API请求封装
  - 请求拦截和响应处理
  - Token认证管理
  - 错误处理和重试机制
  - 图片上传和处理
  - 数据格式化和清洗
- **router.js**: 路由管理和权限控制
  - 登录状态检查
  - 页面跳转封装
  - 白名单管理

## API接口设计

### 用户认证
- `POST /api/v1/user/login` - 用户登录(支持Base64和FormData两种方式)
- `POST /api/v1/user/upload-avatar` - 头像上传

### 食材管理
- `GET /api/v1/ingredients/all` - 获取所有食材
- `GET /api/v1/ingredients/stats` - 获取食材统计信息
- `GET /api/v1/ingredients/most-expiring` - 获取最快过期食材
- `GET /api/v1/ingredients/top-expiring` - 获取最快过期食材列表
- `PUT /api/v1/ingredients/{id}` - 更新食材信息
- `DELETE /api/v1/ingredients/{id}` - 删除食材

### 菜谱推荐
- `GET /api/v1/recipes/recommendations` - 获取菜谱推荐
- `GET /api/v1/recipes/{id}` - 获取菜谱详情
- `GET /api/v1/recipes/match-expiring` - 获取基于临期食材的菜谱推荐

### 图像识别
- `POST /api/v1/food-vision/analyze` - 食材图像识别分析

## 数据存储架构

### 本地存储
- **用户信息**: userInfo, token, tokenExpireTime, userId
- **应用设置**: calorieTarget, expiryReminderTime
- **缓存数据**: 食材信息、菜谱数据临时缓存

### 云端数据
- **用户档案**: 个人信息、健康目标、饮食偏好
- **食材库存**: 实时库存数据、过期状态
- **营养记录**: 每日营养摄入数据
- **菜谱收藏**: 用户收藏的菜谱列表

## 项目配置

### 小程序配置 (app.json)
```json
{
  "pages": [18个页面路径],
  "tabBar": {
    "list": [5个主导航页面]
  },
  "style": "v2",
  "renderer": "webview",
  "componentFramework": "glass-easel",
  "lazyCodeLoading": "requiredComponents"
}
```

### 开发配置 (project.config.json)
```json
{
  "appid": "你的appid",
  "libVersion": "3.7.10",
  "compileType": "miniprogram"
}
```

## 安装与使用

### 环境要求
- 微信开发者工具 (最新版本)
- Node.js 14.0+ (如需本地开发工具)
- 微信小程序基础库 3.0.0+

### 安装步骤
1. 克隆项目到本地
```bash
git clone [项目地址]
cd 食光机-cursor
```

2. 使用微信开发者工具打开项目
   - 打开微信开发者工具
   - 选择"导入项目"
   - 选择项目目录
   - 输入AppID: `你的appid`

3. 配置后端API地址
   - 修改 `utils/api.js` 中的 `BASE_URL` 为实际后端地址
   - 确保后端服务已启动并可访问

4. 预览和调试
   - 在开发者工具中点击"预览"
   - 使用微信扫码在真机上测试

### 权限配置
应用需要以下权限：
- **相机权限**: 用于拍照识别食材
- **相册权限**: 用于选择图片识别
- **网络权限**: 用于API数据交互
- **存储权限**: 用于本地数据缓存

## 开发进度

### ✅ 已完成功能
- [x] 完整的UI界面和交互设计
- [x] 用户登录和认证系统
- [x] 食材智能识别功能
- [x] 库存管理和分类展示
- [x] 菜谱推荐和详情展示
- [x] 营养分析和数据可视化
- [x] 膳食计划管理
- [x] 家庭多成员管理
- [x] 饮食禁忌设置
- [x] 临期食材急救站
- [x] 个人中心和设置
- [x] 组件化开发架构
- [x] API接口集成
- [x] 路由管理和权限控制

### 🚧 待完成功能
- [ ] 自动生成周餐饮计划
- [ ] 一键购物清单生成
- [ ] 菜谱收藏和分享
- [ ] 营养师在线咨询
- [ ] 会员积分系统
- [ ] 数据备份和同步
- [ ] 离线使用模式
- [ ] 性能优化和测试

## 注意事项

### 使用限制
- 需要微信登录授权才能使用完整功能
- 食材识别功能需要网络连接

### 数据安全
- 用户数据采用JWT Token认证
- 敏感信息本地加密存储
- 严格遵循微信小程序安全规范

### 兼容性
- 支持iOS和Android微信客户端
- 基础库版本要求3.0.0及以上
- 响应式设计适配不同屏幕尺寸

## 贡献指南

### 代码规范
- 使用ESLint进行代码检查
- 遵循微信小程序开发规范
- 组件化开发，提高代码复用性
- 使用rpx单位确保响应式设计

### 提交规范
- 功能开发请创建feature分支
- 提交信息请使用中文描述
- 重要更新请更新版本号和文档

## 联系方式

如有问题或建议，请通过以下方式联系：
- 项目Issue: [GitHub Issues]

## 许可证

本项目采用 [MIT License] 开源许可证。

---

**食光机** - 让每一份食材都发光发热，让每一餐都充满智慧！ 🌟

