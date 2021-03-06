# About Module of Google NLP ReadMe:

This is Introduction of how to using Google NLP by my perspective, which is a mainly tutorial that going to use the MVP model of Google NLP Engine to analyze the sentiment of keywords based on we indicated, and utilize it as a part of functionality for Social Media Analyzer.

### MileStone:

**Our milestone are basically divided into three essential part:**
1. Realize what is Google NLP and install the environment.
2. Summary the usage and write the exercise coding to exercise different keywords.  For example, using different words to make the sentiment test by using the engine. (Examples in QuickStart)
3. Define and create the user Stories of our module / application for NLP, and showing how are we going to use them to build something differently and innovation.


# 📝[About the Google NLP itself](https://cloud.google.com/natural-language)

* AutoML Natural Language uses machine learning to analyze the structure and meaning of documents. You train a custom machine learning model to classify documents, extract information, or understand the sentiment of authors.
    * A classification model analyzes a document and returns a list of content categories that apply to the text found in the document.
    * An entity extraction model inspects a document for known entities referenced in the document and labels those entities in the text.
    * A sentiment analysis model inspects a document and identifies the prevailing emotional opinion within it, especially to determine a writer's attitude as positive, negative, or neutral.

The Google Natural Language client Libraries access example of guideline shown at the following:

# 🚦 Interactive API Docs

### [Google NLP QuickStart](https://cloud.google.com/natural-language/automl/docs/quickstart)

* **API Keys Retrieve Example:**

* **Google NLP example**

**Code Example: (in Python)**

```python
# Imports the Google Cloud client library
from google.cloud import language_v1

# Instantiates a client
client = language_v1.LanguageServiceClient()

# The text to analyze
text = u"Dear my love" # Test your own words of sentiment here!
document = language_v1.Document(content=text, type_=language_v1.Document.Type.PLAIN_TEXT)

# Detects the sentiment of the text
sentiment = client.analyze_sentiment(request={'document': document}).document_sentiment

print("Text: {}".format(text))
print("Sentiment: {}, {}".format(sentiment.score, sentiment.magnitude))
```
The above example code is just use Google Auto ML machine learning model to analyze the prevailing emotional attitude in a single word test by normally constructed.

# 💬 Result / Conclusiton

* First, we utilize some example data

![Google NLP Engine test by single label classification](https://user-images.githubusercontent.com/27568828/138531270-48fca193-e990-4745-b399-03f89ca6afa0.png)


![Google NLP Engine test result: Single label classification model: Happiness moment](https://user-images.githubusercontent.com/27568828/138531299-0ac6faad-42a6-46ac-bc12-c41b456a94c8.png)

* Then, we tried to use the installed sentiment analysis NLP model at local to build a single word test demo.
The following graph which showing the text result BASED ON ABOVE CODE.

![Sentiment Analysis Test by using word: " Dear my love"](https://user-images.githubusercontent.com/27568828/138531438-e7401802-a52b-4c2f-824e-05adcb996442.png)

