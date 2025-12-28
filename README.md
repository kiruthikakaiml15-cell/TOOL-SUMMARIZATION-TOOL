#codtechitsolutions-task 1
NAME:KIRUTHIKA K
INTERN ID:CTISO515
**Introduction**
Text summarization is an important application of Natural Language Processing that helps reduce long documents into short and meaningful summaries.
With the increasing amount of digital content, automatic summarization saves time and improves understanding. This project focuses on building a simple text summarization tool using Python.
**Project Overview**
The project aims to summarize lengthy articles by selecting the most important sentences.
It uses a frequency-based approach where frequently occurring words are considered important. Sentences containing these words are given higher priority and included in the summary.
**Methodology**
The input text is first split into sentences. Each word is then analyzed to calculate its frequency.
Sentence scores are computed based on word frequencies. Sentences with the highest scores are selected to generate the final summary.
**Implementation**
The program is implemented using Python without external libraries.
It processes the input text, calculates word frequencies, ranks sentences, and outputs a concise summary along with the original text.
**How the Code Came**
The code is designed based on a frequency-based extractive summarization approach:
Important words appear more frequently
Sentences containing important words are more meaningful
Top-scoring sentences form the summary
This logic is commonly used in basic NLP summarization.
**Full Code Explanation (Step-by-Step)**
Step 1: Function Definition
def summarize_text(text, summary_sentences=2):
Creates a function to summarize text
summary_sentences decides how many lines the summary should have
Step 2: Sentence Splitting
sentences = text.split('.')
Splits the paragraph into individual sentences using full stop
Step 3: Word Frequency Calculation
word_freq = {}
Dictionary to store how often each word appears
for sentence in sentences:
    words = sentence.lower().split()
Converts text to lowercase and splits into words
word_freq[word] = word_freq.get(word, 0) + 1
Increases count for each word
Step 4: Sentence Scoring
sentence_score = {}
Stores importance score of each sentence
sentence_score[sentence] += word_freq[word]
Adds word frequency values to sentence score
Step 5: Sentence Ranking
ranked_sentences = sorted(sentence_score, key=sentence_score.get, reverse=True)
Sorts sentences based on importance (highest first)
Step 6: Summary Generation
summary = ranked_sentences[:summary_sentences]
return '. '.join(summary) + '.'
Selects top sentences and joins them as summary
**Tools & Technologies Used**
Programming Language: Python
Concept: Natural Language Processing
Technique: Frequency-based extractive summarization
**Applications**
This tool can be used in education, news summarization, research articles, and content analysis. 
It is useful for beginners to understand basic NLP concepts.
**Conclusion**
The project successfully demonstrates a simple and effective text summarization technique. 
It reduces lengthy text into a meaningful summary using basic NLP principles and can be further enhanced using advanced libraries and techniques.
