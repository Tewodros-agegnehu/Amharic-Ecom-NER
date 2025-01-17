# EthioMart: Centralized Telegram E-Commerce Hub

## Project Description

EthioMart envisions becoming the leading centralized hub for Telegram-based e-commerce activities in Ethiopia. With the growing reliance on Telegram for business transactions, numerous independent channels have surfaced, leading to challenges in managing product discovery, order placement, and communication across platforms. 

This project addresses these challenges by:

- **Centralizing e-commerce data**: Aggregating real-time data from various Telegram channels into a unified platform.
- **Improving user experience**: Providing customers with seamless access to diverse vendors in one location.
- **Extracting key business data**: Developing a fine-tuned Amharic Named Entity Recognition (NER) system to identify essential entities such as product names, prices, and locations from textual and visual content shared on Telegram.

---

## Key Objectives

### Project Goals:
1. **Real-Time Data Collection**: Extract data from Ethiopian Telegram e-commerce channels in real time.
2. **Advanced NER Model Development**: Tailor models to identify entities including:
   - Product Names or Types
   - Materials or Ingredients
   - Locations
   - Monetary Values or Prices

---

## Tasks Overview

### Task 1: Data Ingestion and Preprocessing

**Objective:** Build a robust system to fetch and preprocess data from multiple Telegram e-commerce channels.

**Steps:**
1. Identify at least five relevant Telegram channels for data extraction.
2. Develop a scraper to collect messages, images, and documents in real time.
3. Preprocess text data by:
   - Tokenizing
   - Normalizing
   - Addressing Amharic-specific linguistic features
4. Clean and organize data into a structured format, separating metadata from message content.
5. Store preprocessed data for subsequent analysis.

### Task 2: Dataset Labeling in CoNLL Format

**Objective:** Label a dataset subset in CoNLL format for NER tasks.

**Entity Types:**
- **B-Product**: Beginning of a product entity.
- **I-Product**: Inside a product entity.
- **B-LOC**: Beginning of a location entity.
- **I-LOC**: Inside a location entity.
- **B-PRICE**: Beginning of a price entity.
- **I-PRICE**: Inside a price entity.
- **O**: Tokens outside any entity.

**Steps:**
1. Annotate 30-50 messages with the above entity labels.
2. Save the annotated data in a plain text file formatted in CoNLL style.

### Task 3: Fine-Tuning the NER Model

**Objective:** Train and fine-tune a multilingual model for Amharic NER.

**Steps:**
1. Select pre-trained models such as XLM-Roberta, BERT-tiny-Amharic, or AfroXMLR.
2. Load the labeled dataset in CoNLL format.
3. Tokenize the data and align labels with the tokenizer’s output.
4. Configure training parameters including:
   - Learning rate
   - Epoch count
   - Batch size
   - Evaluation strategy
5. Use Hugging Face’s Trainer API for fine-tuning.
6. Evaluate model performance using a validation dataset.
7. Save the optimized model for deployment.

### Task 4: Model Comparison and Selection

**Objective:** Evaluate and select the best-performing model for production.

**Steps:**
1. Fine-tune multiple models, including:
   - XLM-Roberta
   - DistilBERT
   - mBERT
2. Compare models based on:
   - Accuracy
   - Speed
   - Robustness when handling multi-modal data
3. Select the model that delivers the best results across evaluation metrics.

### Task 5: Model Interpretability

**Objective:** Foster transparency and trust by interpreting model predictions.

**Steps:**
1. Use tools such as SHAP and LIME to analyze predictions.
2. Investigate difficult cases, such as ambiguous text or overlapping entities.
3. Generate detailed interpretability reports and recommend improvements.

---

## Usage Instructions

### Prerequisites:
- Access to Google Colab or a local environment with GPU support.
- Required libraries:
  - Hugging Face Transformers
  - Datasets
  - Pandas
  - Tokenizers
  - SHAP or LIME (for interpretability)

### Steps to Execute:
1. Clone the repository:
   ```bash
   git clone https://github.com/Tewodros-agegnehu/Amharic-Ecom-NER.git
   cd <repository-folder>
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Follow the tasks outlined above to process data and train the model.
4. Deploy the fine-tuned model for production use.

---

## Contributions

We welcome contributions! Feel free to create a pull request or open an issue to propose enhancements or report bugs.

---

## License

This project is licensed under the MIT License. For more details, refer to the LICENSE file.

---

## Acknowledgments

- **Hugging Face**: Transformers library
- **Telegram Channels**: Source of e-commerce data
- **Open-Source Communities**: Amharic NLP resources

---

## Contact Information

For questions or support, please reach out to: [tewodros.agegnehu@aait.edu.et]

