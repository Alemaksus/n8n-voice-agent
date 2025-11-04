# N8N Voice Agent

A voice-enabled AI agent built with n8n workflow automation.

## Overview

N8N Voice Agent is an experimental project exploring the architecture of an AI-powered voice agent built on the n8n workflow automation platform.

The agent receives a voice input, converts it to text (Speech-to-Text), processes it via LLM API, and generates a spoken response (Text-to-Speech).

This project serves as an R&D sandbox for integrating AI models into voice workflows and designing QA validation methods for dialogs — verifying response accuracy, timing consistency, and speech generation quality.

Planned next step: integrate automated test hooks for validating agent response quality and audio output metrics.

## Project Structure

```
n8n-voice-agent/
├── README.md                    # This file
├── docker-compose.yml           # Docker configuration
├── .env.example                 # Environment variables template
├── /n8n/                       # N8N workflow files
│   └── workflow_voice_agent.json
├── /voice/                     # Voice configuration
│   ├── retell.config.json      # Voice provider config
│   ├── prompt_system.md        # System prompts
│   └── utterances.md           # Sample phrases and escalations
├── /apis/                      # API documentation
│   ├── openmeteo.md            # Weather API docs
│   └── coingecko.md            # Crypto API docs
├── /tests/                     # Test files
│   ├── dialog_scenarios.yaml   # Test scenarios
│   └── e2e_http_tests.py       # HTTP endpoint tests
├── /docs/                      # Documentation
│   ├── architecture.drawio.png # System architecture
│   └── sequence-call.png       # Call flow diagram
└── /demo/                      # Demo materials
    └── demo_script.md          # Demo script
```

## Getting Started

1. Copy `.env.example` to `.env` and configure your environment variables
2. Run `docker-compose up` to start the services
3. Configure your voice provider settings in `/voice/retell.config.json`
4. Import the workflow from `/n8n/workflow_voice_agent.json` into n8n

## Features

- Voice-to-text and text-to-voice processing
- Integration with weather and cryptocurrency APIs
- Configurable prompts and conversation flows
- Comprehensive testing framework
- Docker-based deployment

## Documentation

See the `/docs/` folder for detailed architecture and sequence diagrams.

## Testing

Run the test suite with the files in `/tests/` directory.

