# Travel Planning Agent for LangGraph

This is a sophisticated travel planning agent built with LangGraph and LangChain that integrates with Google Maps API to help users plan trips with natural language.

## Features

- 🗺️ **Google Maps Integration**: Real-time place search and discovery
- 🤖 **Natural Language Understanding**: Plan trips using conversational language
- 🔄 **Human-in-the-Loop**: Approve or reject AI suggestions before applying
- 📍 **Multi-destination Support**: Plan complex itineraries with multiple stops
- 🌐 **Real-time State Management**: Seamless synchronization between agent and UI

## Architecture

The agent consists of 4 main nodes:
- **chat**: Handles conversation and tool orchestration
- **search**: Integrates with Google Maps API for place discovery
- **trips**: Manages trip data with human-in-the-loop approval
- **perform_trips**: Executes approved trip modifications

## Environment Variables

Create a `.env` file with:

```bash
# Required
OPENAI_API_KEY=your-openai-api-key
GOOGLE_MAPS_API_KEY=your-google-maps-api-key

# Optional (for tracing)
LANGCHAIN_TRACING_V2=true
LANGCHAIN_API_KEY=your-langsmith-key
LANGCHAIN_PROJECT=travel-planner
```

## Deployment

This agent is designed to be deployed on LangGraph Platform. The `langgraph.json` file contains all necessary configuration.

## Local Development

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Run the demo:
   ```bash
   python -m travel.demo
   ```

## API Endpoints

Once deployed, the agent exposes standard LangGraph endpoints for interaction with CoPilotKit or other clients.

## License

Part of the CoPilotKit examples collection.
