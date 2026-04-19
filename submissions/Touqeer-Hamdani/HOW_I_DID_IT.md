# How I Did It — Level 2

## What I Did

1. Forked and cloned the lpi-developer-kit repo
2. Ran `npm install` and `npm run build` to set up the project
3. Ran `npm run test-client` — all 8 tests passed (7 tools, one tested twice)
4. Installed Ollama and pulled the qwen3.5:cloud model
5. Ran the example agent (`examples/agent.py`) which connects to the LPI MCP server and feeds results to Ollama
6. Captured all outputs for my submission

## What Problems I Hit

Model mismatch between qwen2.5:1.5b in the examples/agent.py and qwen3.5:cloud model

## What I Learned

- That Ollama runs as a local HTTP API server and the agent just sends POST requests to it
- That the LLM doesn't know about SMILE natively, it only reasons over the context provided
