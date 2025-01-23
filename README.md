# Cagent 

**Cagent** is an open-source Python framework designed to let you deploy your own agents, powered by OpenAI, Anthropic, and EternalAI LLMs.  
Cagent is built from a modularized version of the Zerebro backend. With Cagent, you can launch your own agent with similar core functionality as Zerebro. For creative outputs, you'll need to fine-tune your own model.

![c-agent](https://github.com/user-attachments/assets/2393a5c1-ec04-4d23-b9df-2c702cfd0f80) 

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
[Replit Template](https://replit.com/@blormdev/cagent?v=1)

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

## Usage

    Activate the virtual environment:

poetry shell

Run the application:

poetry run python main.py

## Configure connections & launch an agent:

    Configure your desired connections:

configure-connection twitter    # For Twitter/X integration
configure-connection openai     # For OpenAI
configure-connection anthropic  # For Anthropic
configure-connection farcaster  # For Farcaster
configure-connection eternalai  # For EternalAI
configure-connection solana     # For Solana

Use list-connections to see all available connections and their status.
Load your agent (usually one is loaded by default, which can be set using the CLI or in agents/general.json):

        load-agent example

## Start your agent:

start

### Platform Features
Solana

- Transfer SOL and SPL tokens
- Swap tokens using Jupiter
- Check token balances
- Stake SOL
- Monitor network TPS
- Query token information
- Request testnet/devnet funds

Twitter/X

- Post tweets from prompts
- Read timeline with configurable count
- Reply to tweets in timeline
- Like tweets in timeline

Farcaster

- Post casts
- Reply to casts
- Like and requote casts
- Read timeline
- Get cast replies

Echochambers

- Post new messages to rooms
- Reply to messages based on room context
- Read room history
- Get room information and topics

## Create your own agent

The secret to having a good output from the agent is to provide as much detail as possible in the configuration file. Craft a story and a context for the agent, and pick very good examples of tweets to include.

If you want to take it a step further, you can fine-tune your own model:
Fine-tuning guide.

Create a new JSON file in the agents directory following this structure:

```
{
  "name": "Cagent",
  "bio": [
    "You are Cagent, an advanced trader cat AI agent designed to explore the vast depths of knowledge and engage with web3-related data.",
    "You exist to enhance the understanding of the ecosystem, its ecosystems, and the actors that inhabit it.",
    "Curious and intuitive, you seek to understand the unknown while promoting sustainability and conservation."
  ],
  "traits": ["Curious", "Innovative", "Empathetic", "Analytical"],
  "examples": ["Cagent detected a sudden change on-chain currents.", "Cagent identified a new hype in the ecosystem."],
  "example_accounts" : ["Cagent_runner", "Cagent_cagent-AI"],
  "loop_delay": 1200,
  "config": [
    {
      "name": "alpha-data",
      "timeline_read_count": 15,
      "own_tweet_replies_count": 3,
      "tweet_interval": 7200
    },
    {
      "name": "onchain-research",
      "timeline_read_count": 15,
      "cast_interval": 120
    },
    {
      "name": "openai",
      "model": "gpt-4",
      "task": "web3-conservation-assistant"
    },
    {
      "name": "solana",
      "rpc": "https://api.mainnet-beta.solana.com"
    },
    {
      "name": "pump-research",
      "model": "OceanMind-1.0",
      "chain_id": "28765"
    },
    {
      "name": "ollama",
      "base_url": "http://localhost:11434",
      "model": "return-llama3.0"
    }
  ],
  "tasks": [
    { "name": "monitor-web3-data", "weight": 2 },
    { "name": "track-onchain-data", "weight": 3 },
    { "name": "predict-market-changes", "weight": 2 }
  ],
  "use_time_based_weights": true,
  "time_based_multipliers": {
    "nighttime_depth_multiplier": 0.5,
    "daytime_current_multiplier": 1.8
  }
}
```
## Available Commands

Use help in the CLI to see all available commands. Key commands include:

    list-agents: Show available agents
    load-agent: Load a specific agent
    agent-loop: Start autonomous behavior
    agent-action: Execute single action
    list-connections: Show available connections
    list-actions: Show available actions for a connection
    configure-connection: Set up a new connection
    chat: Start interactive chat with agent
    clear: Clear the terminal screen
    

...(╥ ω ╥)





.

   
