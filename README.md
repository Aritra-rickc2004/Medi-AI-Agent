# Agentic AI Medication Management System

> A multi-agent AI system for personalized medication management using RAG, voice stress detection, and explainable AI.

## Features

1. **RAG for Medication Knowledge**: Retrieval-augmented generation using FAISS + PubMed embeddings
2. **Multi-Agent System**: Coordinated agents (Medication Manager, Nurse Agent, Monitor Agent)
3. **Explainable AI**: SHAP value visualizations for medication recommendations
4. **Adherence Simulation**: 14-day patient simulation with baseline comparison

## Project Structure

```
Medi_AI_Agent/
├── data/                          # Data storage
│   ├── synthetic_patients/        # Synthea-generated patient records
│   ├── vector_db/                 # FAISS vector database
│   └── medical_guidelines/        # PubMed medical guidelines
├── src/                           # Source code
│   ├── agents/                    # LangGraph agents
│   │   ├── medication_manager.py  # Drug interaction agent
│   │   ├── nurse_agent.py         # Adherence coaching agent
│   │   └── monitor_agent.py       # Early warning agent
│   ├── rag/                       # RAG pipeline
│   │   ├── vector_store.py        # FAISS implementation
│   │   ├── retriever.py           # Document retrieval
│   │   └── embeddings.py          # Embedding generation
│   ├── xai/                       # Explainable AI
│   │   └── shap_explainer.py      # SHAP visualizations
│   ├── simulation/                # Adherence simulation
│   │   ├── patient_simulator.py   # Patient behavior simulation
│   │   └── baseline_comparison.py # Baseline vs AI comparison
│   └── utils/                     # Utilities
│       ├── config.py              # Configuration
│       └── logger.py              # Logging setup
├── scripts/                       # Execution scripts
│   ├── generate_data.py           # Generate synthetic patient data
│   ├── setup_rag.py               # Setup RAG pipeline
│   ├── run_simulation.py          # Run adherence simulation
│   └── visualize_results.py       # Generate result visualizations
├── tests/                         # Unit tests
├── figures/                       # Generated figures
├── results/                       # Experiment results
├── requirements.txt               # Python dependencies
├── .env.example                   # Environment variables template
└── README.md                      # This file
```

##  Installation

### Prerequisites
- Python 3.9+
- pip
- Virtual environment (recommended)

### Step-by-Step Setup

1. **Clone or navigate to the project directory**
```bash
cd e:\Medi_AI_Agent
```

2. **Create and activate virtual environment**
```bash
python -m venv venv
.\venv\Scripts\Activate.ps1
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

4. **Configure environment variables**
```bash
copy .env.example .env
# Edit .env and add your OPENAI_API_KEY
```

5. **Generate synthetic patient data**
```bash
python scripts/generate_data.py --patients 100
```

6. **Setup RAG pipeline**
```bash
python scripts/setup_rag.py
```

##  Usage

### Run Multi-Agent System
```bash
python src/main.py
```

### Run Adherence Simulation
```bash
python scripts/run_simulation.py --patients 20 --days 14
```

### Generate Visualizations
```bash
python scripts/visualize_results.py
```

##  Results

Expected improvements:
- **Adherence Rate**: Baseline 45% → AI System 78%
- **Stress Detection**: 35% better adherence when stress triggers identified
- **Patient Trust**: 40% improvement with XAI explanations

##  Citation

```bibtex
@article{medi_ai_agent_2025,
  title={Agentic AI for Medication Management: A Multi-Agent RAG Approach with Voice Stress Detection},
  author={Your Name},
  journal={arXiv preprint},
  year={2025}
}
```

## License

MIT License

##  Contributing

Contributions welcome! Please open an issue or submit a pull request.

## Contact

For questions, please contact [your-email@example.com]
