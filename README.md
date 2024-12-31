# Machine Learning for Lyrics: Artist Prediction

This project applies machine learning and natural language processing techniques to identify the artist of a song based on its lyrics. By utilizing a **Bag of Words Model** and a **Log Probability Equation**, the program is trained to make predictions about song authorship with notable accuracy.

## Project Overview

The primary goal of this project is to explore the use of natural language processing in distinguishing musical artists based on their lyrical styles. The program is trained on song lyrics from top-streamed artists and uses probabilities to predict the artist for new, unseen lyrics.

## Features

- **Natural Language Processing:** Uses a Bag of Words Model to represent songs.
- **Training Dataset:** Trained on lyrics from popular songs by five top-streamed artists.
- **Prediction Algorithm:** Utilizes a log probability formula to calculate the likelihood of an artist being associated with given lyrics.
- **Evaluation Metrics:** Outputs accuracy metrics based on test predictions.

## How It Works

### Bag of Words Model
The program treats each song as a "bag of words," ignoring word order and focusing solely on the presence of words. Key data collected during training includes:
- Total number of songs in the training set.
- Number of unique words in the training set.
- Word occurrences across songs and labels (artists).

### Log Probability Formula
The algorithm calculates the probability of a label (artist) given the lyrics using the formula:
ln P(C) + ln P(W1 | C) + ln P(W2 | C) + ... + ln P(Wn | C)

where:
- `ln P(C)` is the natural log of the prior probability of label `C`.
- `ln P(W | C)` is the conditional probability of a word `W` appearing under label `C`.

### Training Dataset
The training set includes the top ten most streamed songs for each of the following artists:
- **Drake**
- **Bad Bunny**
- **Taylor Swift**
- **The Weeknd**
- **Ed Sheeran**

### Test Dataset
Three personal favorite songs per artist were used to evaluate the model's performance.

## Results

- **Accuracy:** The algorithm correctly identified the artist for 10 out of 15 test songs (67% accuracy).
- **Observations:**
  - The program successfully identified all songs by **Drake** and **Bad Bunny**.
  - Songs by **Taylor Swift** and **Ed Sheeran** were sometimes misclassified as **Drake**, likely due to stylistic similarities in word choice.
  - Misclassifications between **The Weeknd** and **Drake** occurred, reflecting their shared vocabulary.

## Improvements

The following enhancements are suggested to improve prediction accuracy:
1. **Incorporate unique buzzwords:** Reduce probabilities for words strongly associated with specific artists.
2. **Integrate musical features:** Use rhythm, tempo, and instrumentation data alongside lyrics.

## Setup and Usage

1. **Prerequisites:** Python 3.x with necessary libraries for data handling and processing.
2. **Prepare Data:** Include the CSV file with training and test datasets.
3. **Run the Program:**
   ```bash
   python artist_predictor.py
4. **Output:** Predictions for test songs along with accuracy metrics.

## Acknowledgements
This project builds on a machine learning assignment originally developed for EECS 280 at the University of Michigan. Special thanks to:

Andrew DeOrio and James Juett for the original project specifications.
Amir Kamil for contributions to code structure and implementation.
The project was initially designed to predict the topic of Piazza posts and has been adapted to identify artists based on song lyrics.

## License
This project is for educational and non-commercial use only. Adaptations and insights are credited to the original authors and contributors.