# Fine-Tuning LLM

Base model: [DistilBERT](https://huggingface.co/distilbert/distilbert-base-uncased) from Hugging Face<br>
Dataset: Hugging Face [IMDb dataset](https://huggingface.co/datasets/stanfordnlp/imdb)<br>
>A random sample of 1000 points each was taken from the train and test data.

Accuracy is used to track model metrics.<br>
The model is fine tuned using LoRA PEFT on Google Colab GPU instance.<br>

**Model training metrics**:<br>
|Epoch|	Training Loss|	Validation Loss|	Accuracy|
|---|---|---|---|
|1|	No log|	0.479512	|{'accuracy': 0.85}|
|2|	0.413100|	0.652610|	{'accuracy': 0.851}|
|3|	0.413100|	0.676640|	{'accuracy': 0.854}|
|4|	0.201700|	0.959733|	{'accuracy': 0.855}|
|5|	0.201700|	0.962337|	{'accuracy': 0.857}|
|6|	0.110200|	0.984152|	{'accuracy': 0.866}|
|7|	0.110200|	1.194281|	{'accuracy': 0.859}|
|8|	0.023000|	1.287383|	{'accuracy': 0.859}|
|9|	0.023000|	1.315396|	{'accuracy': 0.859}|
|10|	0.004700|	1.312917|	{'accuracy': 0.86}|

### Model results on sample texts
**Before**
It was good. - Positive
Not a fan, don't recommed. - Positive
Better than the first one. - Positive
This is not worth watching even once. - Positive
This one is a pass. - Positive

**After**
It was good. - Positive
Not a fan, don't recommed. - Negative
Better than the first one. - Positive
This is not worth watching even once. - Negative
This one is a pass. - Negative

---

### References
Huge shoutout to [Shaw Talebi](https://www.youtube.com/@ShawhinTalebi/featured)<br>
References:
1. [Fine-tuning Large Language Models (LLMs) | w/ Example Code](https://www.youtube.com/watch?v=eC6Hd1hFvos) by Shaw Talebi
1. Shaw Talebi [GitHub](https://github.com/ShawhinT/YouTube-Blog/tree/main/LLMs/fine-tuning)
