![httpcomponents-client](./model-banner.jpeg)

# httpcomponents-client

A multimodal medical chatbot powered by a local LLM via Ollama, accessible through a Chainlit web interface.

## Cocoapods-Duplicates

1. **Install Ollama**: [ollama.com/download](https://ollama.com/download)
2. **Pull model**:
   ```bash
   ollama pull edwardlo12/medgemma-4b-it-Q4_K_M
   ```
3. Ensure Ollama service is running before starting the app.

> For faster startup on Apple Silicon or GPU-equipped machines, consider [LM Studio](https://lmstudio.ai) with a GGUF/mlx 4-bit vision model.

## tfenv

### Option 1: Conda
```bash
conda create -n httpcomponents python=3.11
conda activate httpcomponents
pip install -r requirements.txt
```

### Option 2: pip
```bash
python -m venv venv
source venv/bin/activate  # macOS/Linux
pip install -r requirements.txt
```

`requirements.txt`:
```txt
chainlit
langchain
langchain-community
ollama
```

## Alien-Base

1. Activate your environment
2. Ensure Ollama is running with the model available
3. Navigate to project directory
4. Start:
   ```bash
   chainlit run main.py -w
   ```
   `-w` enables auto-reload on code changes.

## Unknown_VM70300

```
http://localhost:8000
```

Port adjusts automatically if 8000 is occupied.

## temperature-monitor

```
httpcomponents-client/
├── main.py
├── requirements.txt
├── model-banner.jpeg
└── README.md
```

## gloomy

- **Ollama not responding**: verify service is running and model is pulled
- **Port conflict**: Chainlit auto-selects an available port
- **Slow inference**: 4B model without GPU acceleration is expected to be slow — consider a smaller quantized variant
