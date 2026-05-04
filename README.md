# AI Chatbot

A plug-and-play AI chatbot widget for website integration. Supports multiple backends — **Claude API**, **OpenAI API**, and **NVIDIA NIM** (Gemma, Llama, Mistral, etc.) — with a single `<script>` tag embed.

## Planned Features
- [ ] Floating chat widget (toggle open/close)
- [ ] Multi-backend support: Claude · OpenAI · NVIDIA NIM
- [ ] Custom system prompt via `data-` attribute
- [ ] Conversation history (session-based)
- [ ] Typing indicator animation
- [ ] Mobile-responsive, themeable via CSS variables
- [ ] Easy embed: one `<script>` tag, no build step
- [ ] Rate limiting & input sanitisation

## Tech Stack
- Vanilla JavaScript (zero dependencies)
- CSS (themeable via CSS variables)
- Claude API / OpenAI API / NVIDIA NIM API

## NVIDIA NIM Integration

NVIDIA NIM gives free-tier access to hosted LLMs (Gemma, Llama 3, Mistral, etc.) via an OpenAI-compatible endpoint.

```python
# Example: calling NVIDIA NIM with Gemma 3
import requests

response = requests.post(
    "https://integrate.api.nvidia.com/v1/chat/completions",
    headers={"Authorization": f"Bearer {API_KEY}"},
    json={
        "model": "google/gemma-3n-e4b-it",
        "messages": [{"role": "user", "content": "Hello!"}],
        "max_tokens": 512,
        "temperature": 0.20
    }
)
```

> Store your API key in an environment variable or `.env` file — **never hardcode it in source code.**

## Usage (planned)
```html
<script
  src="chatbot.js"
  data-backend="nvidia"
  data-model="google/gemma-3n-e4b-it"
  data-prompt="You are a helpful assistant."
></script>
```

## Configuration (`.env.example`)
```
CLAUDE_API_KEY=your_claude_key_here
OPENAI_API_KEY=your_openai_key_here
NVIDIA_API_KEY=your_nvidia_nim_key_here
```

## Status
> In development — initial commit coming soon.

---
*Part of the [B-star51 AI/Automation portfolio](https://github.com/B-star51)*