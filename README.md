# Fikira-Chatbot

# **Fikira - Mental Health FAQ Chatbot**

Welcome to **Fikira**, your friendly and reliable virtual assistant designed to answer mental health-related queries! Fikira is powered by natural language processing (NLP) and a robust FAQ dataset to provide accurate and relevant answers. Whether you're seeking mental health advice or simply need to understand common concepts better, Fikira is here to assist.

## **Features**

- **Natural Language Understanding**: The chatbot uses **NLTK** for text tokenization, stopword removal, and lemmatization to improve accuracy in understanding user queries.
- **FAQ Matching**: Fikira finds the best matching FAQ answer using keyword-based techniques.
- **Concise Answers**: For brevity, responses are limited to 3 sentences, making it easy to understand key information quickly.
- **Related Question Suggestions**: If you're not satisfied with the answer, Fikira provides related questions to explore further.

## **How it Works**

1. **Preprocessing**: When you input a question, the system tokenizes, removes stopwords, and lemmatizes the sentence for better analysis.
2. **Keyword Matching**: It identifies the most relevant FAQ based on keyword intersections between your query and the FAQ questions.
3. **Answer Generation**: The chatbot returns the most relevant answer, limited to 3 sentences, and suggests related questions for further exploration.

## **Dependencies**

To run this chatbot, you'll need the following libraries installed:

- `pandas` - for data manipulation
- `nltk` - for text processing
- `ipywidgets` - for interactive widgets in Jupyter/Colab
- `IPython` - for displaying widgets in Jupyter/Colab

Ensure you've installed these dependencies by running:

```bash
pip install pandas nltk ipywidgets
```

Additionally, make sure to download the necessary **NLTK resources** by running:

```python
import nltk
nltk.download('punkt', quiet=True)
nltk.download('stopwords', quiet=True)
nltk.download('wordnet', quiet=True)
```

## **How to Use**

1. **Load Your FAQ Data**: Prepare a CSV file containing at least two columns:
   - `Question` - the user's query.
   - `Answer` - the corresponding answer to the query.

2. **Run the Chatbot**: After loading the data, simply type in your question, and Fikira will provide an accurate and concise response.

3. **Interact**: For a smooth interaction, use the provided text input box to ask questions and get immediate responses. Suggestions for related questions will appear if further information is needed.

## **Interactive Mode**

The chatbot can be used in an interactive mode (via Jupyter/Colab) with easy-to-use widgets for a seamless experience. Input your query, and Fikira will respond with the most relevant answers and offer related questions for better exploration.

## **Customization**

- **Adjusting Response Length**: The current configuration limits responses to 3 sentences. This can be customized in the code to meet your requirements.
- **Update FAQ Dataset**: To change the FAQ content, simply update the `Mental_Health_FAQ.csv` file with new or revised questions and answers.
  
## **Contribution**

Fikira is open for contributions! If you'd like to improve its functionality or add more features, feel free to fork this repository and create a pull request. Contributions such as fixing bugs, adding more FAQs, or improving the NLP models are welcome.

## **License**

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

### **Example Usage**:

```python
faq_questions, faq_answers = load_faq_data("Mental_Health_FAQ.csv")
if faq_questions and faq_answers:
    widget_mode(faq_questions, faq_answers)
else:
    print("⚠️ Failed to load FAQ data.")
```

For more details on how the FAQ data is structured and how to prepare it, check the documentation inside the repo.

---

Let me know if you'd like to add or adjust any sections!
