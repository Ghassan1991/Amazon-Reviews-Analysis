# Amazon Reviews Sentiment Analysis

## 🚀 Overview
This project builds and serves a sentiment analysis model on Amazon product reviews using:
- Data wrangling & EDA (pandas, sklearn)
- Text preprocessing (spaCy, NLTK)
- Classic ML (Logistic Regression)
- LLM Fine-tuning (DistilBERT via Hugging Face Transformers)
- Model API with FastAPI

## 📂 Dataset
- **Source:** [Amazon Polarity Dataset](https://huggingface.co/datasets/amazon_polarity)
- 20,000 sample reviews, labeled as positive or negative.

## 📊 Project Steps
1. **Data Wrangling & EDA:** Load, clean, and explore Amazon review data.
2. **Text Preprocessing:** Tokenization, stopword removal, lemmatization.
3. **Classic ML:** Train/test with Logistic Regression, evaluate metrics.
4. **LLM Fine-Tuning:** Fine-tune DistilBERT for sentiment classification.
5. **Model Serving:** Deploy via FastAPI (local API).

## 🛠️ Requirements
- Python 3.9+
- `pandas`, `scikit-learn`, `spaCy`, `nltk`
- `torch`, `transformers`
- `fastapi`, `uvicorn`

> Install requirements with:  
> `pip install -r requirements.txt`

## 🏃‍♂️ How to Run

1. **Train & Fine-tune:**  
   Run the notebook `Data_Wrangling_and_finetune.ipynb` (Colab or Jupyter).

2. **Serve the Model Locally:**
   - Download/export the `finetuned_distilbert` folder into your repo.
   - Start FastAPI:
     ```bash
     uvicorn serve_model:app --reload
     ```
   - Visit [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs) for the interactive API docs.

3. **Sample API Request:**
   - POST to `/predict`:
     ```json
     {
       "text": "I love this product! Works great."
     }
     ```
   - Response:
     ```json
     {
       "result": [{"label": "LABEL_1", "score": 0.98}]
     }
     ```


## 🙋‍♂️ Author
Ghassan Alkahlout

## 📚 References
- [Amazon Polarity Dataset](https://huggingface.co/datasets/amazon_polarity)
- [Hugging Face Transformers](https://huggingface.co/docs/transformers/index)
- [spaCy Documentation](https://spacy.io/usage)
- [FastAPI Docs](https://fastapi.tiangolo.com/)

---

## ✅ Next Steps

- Try LoRA/QLoRA fine-tuning for larger models.
- Move to Fake News Detection as next project.
- Experiment with deployment (Docker, CI/CD) and agentic workflows.

