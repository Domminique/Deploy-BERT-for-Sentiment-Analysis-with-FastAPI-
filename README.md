  

# Deploy a pre-trained BERT model for Sentiment Analysis as a REST API using FastAPI

## Demo

The model is trained to classify sentiment (negative, neutral, and positive) on a custom dataset from app reviews on Google Play. Here's a sample request to the API:

```bash
http POST http://127.0.0.1:8000/predict text="Good basic lists, i would like to create more lists, but the annual fee for unlimited lists is too out there"
```

The response you'll get looks something like this:

```js
{
    "confidence": 0.9999083280563354,
    "probabilities": {
        "negative": 3.563107020454481e-05,
        "neutral": 0.9999083280563354,
        "positive": 5.596495248028077e-05
    },
    "sentiment": "neutral"
}
```

You can also [read the complete tutorial here](https://www.curiousily.com/posts/deploy-bert-for-sentiment-analysis-as-rest-api-using-pytorch-transformers-by-hugging-face-and-fastapi/)
  
  
# What is sentiment analysis and how can machine learning help Kafunge customers?
  
 When you think of artificial intelligence (AI), the word “emotion” doesn’t typically come to mind. But there’s an entire field of research using AI to understand emotional responses to news, product experiences, movies, restaurants, and more. It’s known as sentiment analysis, or emotion AI, and it involves analyzing views – positive, negative or neutral – from written text to understand and gauge reactions.\n",
    
    
 The tech behind sentiment analysis involves **natural language processing or linguistic** algorithms that assign values to positive, negative or neutral text (converting opinions into datasets), while machine learning processes the datasets to reveal relevant trends over time. There’s significant planning required: How do you ensure the algorithms capture useful information? Are you identifying the right phrases to analyze? How can you convert findings into better products, services, and experiences?\n
    
# Goal Defination
    
 Our ojective in this tutorial will be to Identify the next best action for the customerthrough real-time insights that incorporate machine learning tools— sentiment analysis—can help **Kafunge**, **an inside sales CRM for SMEs and Startu-up** assess the likelihood of a deal closing or the level of a customer’s loyalty. I believe that Personally-tailored recommendations powered by machine learning can engage and delight customers with information and offers that are relevant to them
    
 # Sentiment Analysis with BERT and Pytorch
    
 ## Pytorch
    
In my humble opinion, PyTorch is the sweet way to solve Machine Learning problems, in the real world! The vast community allows you to work state-of-the-art models and deploy them to production in no time (relatively speaking).Almost every framework is great, but PyTorch has really solid roots. Easy to use and understand, allows for fast experimentation and standard debugging tools apply! Enjoy!
    
## BERT
In this tutorial, you'll learn how to fine-tune BERT for sentiment analysis. You'll do the required text preprocessing (special tokens, padding, and attention masks) and build a Sentiment Classifier using the amazing Transformers library by Hugging Face!\n",
    
You'll learn how to:
   
-Intuitively understand what BERT is
- Preprocess text data for BERT and build PyTorch Dataset (tokenization, attention masks, and padding)
- Use Transfer Learning to build Sentiment Classifier using the Transformers library by Hugging Face
- Evaluate the model on test data




## Installation

Clone this repo:

```sh
git clone git@github.com:curiousily/Deploy-BERT-for-Sentiment-Analysis-with-FastAPI.git
cd Deploy-BERT-for-Sentiment-Analysis-with-FastAPI
```

Install the dependencies:

```sh
pipenv install --dev
```

Download the pre-trained model:

```sh
bin/download_model
```

## Test the setup

Start the HTTP server:

```sh
bin/start_server
```

Send a test request:

```sh
bin/test_request
```

## License

MIT
