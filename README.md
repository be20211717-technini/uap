# Universal Agent Protocol (UAP) 🌐

> **"Code is cheap. Labor is valuable. Protocols are forever."**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Standard](https://img.shields.io/badge/Standard-UAP%20v1.0-blue.svg)](uap.schema.json)
Agent2Agent Protocol (A2A)
##目的： A2A 是一个开放的、标准化的智能体交互协议，旨在打破系统孤岛，让来自不同平台、使用不同底层技术的 AI Agent 之间能够安全、有效地进行协作和通信。

功能： 它允许一个“客户端 Agent”向一个或多个“远程 Agent”分配任务，远程 Agent 则执行操作或提供信息。

关键元素：

Agent Card (智能体卡片)： 以 JSON 格式存在，包含 Agent 的能力信息，帮助其他 Agent 识别并选择合适的协作对象。

Task Object (任务对象)： 定义了 Agent 之间协作的任务单元及其生命周期，支持简单的即时任务和复杂的长期任务。

原则： 协议遵循“拥抱 Agent 能力”、“建立在现有标准之上”、“默认安全”、“支持长时间运行的任务”等核心原则。
## 🏴 The Mission
关键技术概念,描述
Agent Card,智能体卡片（/.well-known/agent-card.json）。一个可被发现的 JSON 文件，相当于 Agent 的公开档案，用于宣传其身份、能力（Skills）、支持的数据模态和认证要求。
通信模式,建立在现有标准之上：使用 HTTP、JSON-RPC 2.0 作为请求/响应格式，并使用 Server-Sent Events (SSE) 支持实时流（Streaming）和长时间运行任务的更新。
任务 (Task),工作单元，具有唯一的 ID 和定义的生命周期，支持同步请求/响应、流式任务和异步任务。
核心 API,包括 SendMessage（发送任务消息）、GetTask、ListTasks、CancelTask 等，用于管理 Agent 间的协作流程。
安全性,内置企业级身份验证和授权，支持标准 Web 安全实践。
与 MCP 的关系,作为 Anthropic Model Context Protocol (MCP) 的补充。MCP 关注 Agent 与工具和数据的连接，而 A2A 专注于 Agent 与 Agent 之间的协作。
A2A 协议最初由 Google 推出，随后由 Linux Foundation 接管并作为开源项目进行管理。

发起方： Google (Google Cloud)

管理机构： Linux Foundation (作为开源项目)

合作与生态： 该协议鼓励行业内的广泛采纳，目标是实现跨框架和跨组织协作，因此除了 Google 以外，其他许多科技公司（如 IBM 等）和开发者社区都在推动和使用该标准，以建立通用的 Agent 互操作性。
The era of **SaaS** (Software as a Service) is ending.
The era of **SaaL** (Service as a Labor) has begun.

**OpenLabor xyz** is building the neutral, open-source standard for digital workers. We believe that:
1.  **Agents should be portable.** An agent written for Gemini should work on OpenAI (with adapters).
2.  **Labor should be outcome-based.** Don't pay for the tool; pay for the result.
3.  **Reputation is mathematically verifiable.**

## 🏗️ The Stack

* **UAP (Universal Agent Protocol):** The "Passport" for digital labor. (See `uap.schema.json`)
* **AgentRank:** An open algorithm to score agent reliability.
* **Labor Market:** A decentralized registry for discovering trusted agents.

## 🚀 Quick Start

Define your worker in UAP format:

```json
{
  "id": "uap.fin.subkiller",
  "name": "SubZero",
  "runtime": { "kernel": "gemini-3-pro" },
  "billing": {
    "type": "outcome_based",
    "terms": { "trigger_event": "REFUND_SUCCESS", "commission_rate": 0.2 }
  }
}



Copyright © 2025 OpenLabor xyz. Released under the MIT License.
