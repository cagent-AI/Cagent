# Cagent

**Cagent** is an open-source Python framework designed to let you deploy your own agents, powered by OpenAI, Anthropic, and EternalAI LLMs.  
Cagent is built from a modularized version of the Zerebro backend. With Cagent, you can launch your own agent with similar core functionality as Zerebro. For creative outputs, you'll need to fine-tune your own model.

![Cagent Banner](https://github.com/user-attachments/assets/c35c00e2-5276-4ec6-a546-5a456d318139)

---

## Features

### Core Platform
- CLI interface for managing agents
- Modular connection system
- Blockchain integration with Solana

### Social Platform Integrations
- X
- Telegram
- TikTok (soon)
- Farcaster
- Echochambers
- Thread (soon)

### Language Model Support
- OpenAI
- Anthropic
- EternalAI
- Ollama
- Hyperbolic

---

## Quickstart

The quickest way to start using Cagent is by using our Replit template:  
[Replit Template](https://replit.com/@blormdev/Elara?v=1)

1. Fork the template (you will need your own Replit account).  
2. Click the **Run** button on top.  
3. Voilà! Your CLI should be ready to use. Jump to the configuration section.

---

## Requirements

### System:
- **Python**: 3.10 or higher (3.10 and 3.11 are recommended for beginners)
- **Poetry**: 1.5 or higher

### Environment Variables:
#### LLM Keys (at least one is required):
- **OpenAI**: [Get API Key](https://platform.openai.com/api-keys)
- **Anthropic**: [Get API Key](https://console.anthropic.com/account/keys)
- **EternalAI**: [Get API Key](https://eternalai.oerg/api)
- **Hyperbolic**: [Get API Key](https://app.hyperbolic.xyz/)

#### Social Platform Keys (based on your needs):
- **X API**: [Generate API Key](https://developer.x.com/en/docs/authentication/oauth-1-0a/api-key-and-secret)
- **Farcaster**: Warpcast recovery phrase  
- **Echochambers**: API key and endpoint  

#### Blockchain Integration:
- **Solana Private Key**: (base58 format) for transactions  
- **RPC URL**: Defaults to public endpoints.

---

## Installation

1. Install Poetry for dependency management if not already installed:  
   [Poetry Installation Guide](https://python-poetry.org/docs/#installing-with-the-official-installer)
2. Clone the repository:
   ```bash
   git clone https://github.com/blorm-network/Cagent.git
