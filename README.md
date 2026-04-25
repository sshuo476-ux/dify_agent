# FindBest EV Agent

## 中文说明

FindBest EV Agent 是一个基于 AI Agent 的新能源汽车推荐系统。用户可以输入购车诉求，系统会从新能源汽车数据库中检索匹配车型；如果库内信息不足，Agent 会通过联网搜索补全资料，并支持将用户感兴趣的车型加入收藏，以及通过飞书 Webhook 推送销售线索。

## 核心流程

### 1. 填写需求，获得个性化推荐

开始对话前，用户需要先输入基本诉求，例如用车场景、购车预算、期望车型（SUV 或轿车），以及对智能驾驶的具体要求。

随后，Agent 会在新能源汽车数据库中检索，并给出匹配度较高的推荐车型。

### 2. 库内无结果，联网检索补全信息

如果用户想了解的车型在数据库里没有，聊天过程中 Agent 会自动调用 Perplexity 进行全网搜索，并返回该车型的权威资料与关键信息。

这样可以保证推荐过程不会因为库内数据不足而中断。

### 3. 感兴趣车型加入喜欢列表

当用户对某个车型产生兴趣时，Agent 会把它自动加入用户的喜欢列表（Favorites），并存入用户侧数据库。

这个列表可以作为后续购车备选清单，方便用户进行对比、复盘和决策。

### 4. 销售线索收集与飞书 Webhook 通知

这个 Agent 的核心目标之一，是帮助新能源汽车销售团队更早、更准确地了解用户需求。

在对话中，Agent 会适时询问用户是否需要一对一服务。若用户同意并留下手机号，系统会通过飞书（Lark）Webhook 将线索以机器人消息的形式推送到销售群，方便销售同学及时跟进。

## 技术栈

- Next.js
- React
- TypeScript
- Tailwind CSS

## 本地运行

安装依赖：

```bash
pnpm install
```

启动开发服务器：

```bash
pnpm dev
```

构建生产版本：

```bash
pnpm build
```

## 项目结构

- `app/` - Next.js 路由与全局样式
- `components/` - 可复用 UI 组件与页面模块
- `public/` - 静态图片资源
- `lib/` - 公共工具函数

---

## English

FindBest EV Agent is an AI-powered new energy vehicle recommendation system. It helps users describe their car-buying needs, retrieves matching vehicles from a structured EV database, supplements missing information through web search, and supports sales lead collection through Lark webhook notifications.

## Core Flow

### 1. Fill in needs, then get personalized recommendations

Before the conversation starts, users provide their basic requirements, such as usage scenario, purchase budget, preferred body type, and intelligent driving requirements.

The Agent then searches the new energy vehicle database and recommends models with a high matching score.

### 2. No result in database, then search online

If a model or requirement is not covered by the internal database, the Agent automatically calls Perplexity during the conversation to search the web and return authoritative information and key details.

This keeps the recommendation experience continuous even when the local database does not contain enough information.

### 3. Interested models are added to Favorites

When users show interest in a vehicle, the Agent can automatically add it to the user's Favorites list and save it in the user-side database.

This creates a shortlist for later comparison, review, and purchase decision-making.

### 4. Sales lead collection with Lark webhook notification

One of the core goals of this Agent is to help new energy vehicle sales teams understand user needs earlier and more accurately.

During the conversation, the Agent can ask whether the user wants one-on-one service. If the user agrees and leaves a phone number, the system sends the lead information to a sales group through a Lark webhook as a bot message, so the sales team can follow up in time.

## Tech Stack

- Next.js
- React
- TypeScript
- Tailwind CSS

## Getting Started

Install dependencies:

```bash
pnpm install
```

Start the development server:

```bash
pnpm dev
```

Build for production:

```bash
pnpm build
```

## Project Structure

- `app/` - Next.js app routes and global styles
- `components/` - Reusable UI and page sections
- `public/` - Static image assets
- `lib/` - Shared utilities

