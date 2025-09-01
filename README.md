# ai-systems-data-engineering
Data engineering + ML systems: lakehouse/ETL, streaming, feature store, MLOps, and model serving. Synthetic data → train → ONNX → FastAPI service + CI.
# AI Systems & Data Engineering
**Goal:** end-to-end, reproducible ML systems: ingest → validate → transform → feature store → train → export (ONNX) → serve (FastAPI) → CI.

## Quickstart
```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python etl/synth_data.py
python etl/transform.py
python etl/validate.py
python training/train.py
python training/export_onnx.py
uvicorn serving.app:app --reload
