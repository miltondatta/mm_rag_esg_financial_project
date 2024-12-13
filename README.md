# mm_rag_esg_financial_project
Multimodal ESG Financial Analysis RAG Application

## To download a model from Huggingface HUb, Follow these steps

```bash
sudo apt install git-lfs
```
Default Model download directory is ~/.cache/huggingface. To change the default directoru use `cache_dir` option in the download option like below:

```bash
from transformers import AutoTokenizer, AutoModelForSeq2SeqLM
```
```bash
model_name = "facebook/bart-large-cnn"
```
### Download the tokenizer
```bash
tokenizer = AutoTokenizer.from_pretrained(model_name,cache_dir="/home/pms/llm_project/mm_rag_esg_financial_project/saved_model")
```
### Download the summarization model
```bash
model = AutoModelForSeq2SeqLM.from_pretrained(model_name,force_download=True,cache_dir="/home/pms/llm_project/mm_rag_esg_financial_project/saved_model")
```