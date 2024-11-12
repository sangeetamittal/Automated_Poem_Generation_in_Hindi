# Automated_Poem_Generation_in_Hindi

**Data Pre-processing**:  

I have did some pre-processing in starting for learning purpose for this project. It includes-  
1. Tokenization
2. Stopwords removal
3. Lemmatization
4. POS tagging using Spacy
   
Some other pre-processing steps that we can do on English (or other) dataset are-
1. Converting to lowercase
2. Stemming

The **methodology** used for Hindi Poem Generation includes:

**Data Preparation:**

Additional poems are loaded from a dataset stored in multiple files within a specified directory, creating a DataFrame to store and organize the poems for training.

**Language Model Setup and Training:**

The FastAI library is used to build a language model using the AWD_LSTM architecture, which is effective for text generation tasks.
A DataBlock is created, specifying a text block and random data split with 20% reserved for validation.
The model is fine-tuned using fit_one_cycle for three epochs, with learning rates identified via the learning rate finder.

**Text Generation:**

After training, the model generates new lines of poetry by predicting a sequence of words based on a starting word (e.g., "बादल" or "खुशियाँ") and producing a continuation of the theme.
This approach combines NLP preprocessing, a structured data pipeline, and a neural language model to generate poetry in Hindi based on an initial prompt.
