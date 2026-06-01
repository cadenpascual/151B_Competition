# CSE 151B Competition - Qwen3 Math Fine-Tuning

## Hardware & Performance
* **GPU Used:** NVIDIA A30 (via DSMLP Cluster)
* **Approximate Training Time:** ~4.5 hours for Stage 2 GRPO, ~5 hours for Stage 1 SFT
* **Approximate Inference Time:** ~1 hour for the private test set.

## Setup Instructions
No local weights need to be downloaded. The `run_inference()` function will automatically download the fine-tuned LoRA adapters and base model directly from Hugging Face. Ensure your environment has the following installed:
`pip install unsloth torch pandas tqdm datasets trl transformers`

## How to Reproduce Results
Simply execute the Jupyter Notebook `run_inference.ipynb` or call the function directly from the script:
```python
from run_inference import run_inference
run_inference(
    model_path="your-hf-username/qwen-math-151b-champion", 
    test_data_path="data/private.jsonl", 
    output_csv_path="submission.csv"
)
