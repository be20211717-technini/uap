# Universal Agent Protocol (UAP) 🌐

> **"Code is cheap. Labor is valuable. Protocols are forever."**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Standard](https://img.shields.io/badge/Standard-UAP%20v1.0-blue.svg)](uap.schema.json)

## 🏴 The Mission

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
