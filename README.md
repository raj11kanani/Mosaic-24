


# Hangman Game Prediction Using N-Gram Models

## Overview
This project implements a statistical model to predict words and play the Hangman game using N-Gram techniques. The model uses unigrams, bigrams, trigrams, and four-grams to predict the next letter in a word based on the letters guessed so far.

## Project Structure
- **Data and Preprocessing**: Handles loading and processing the dataset of words.
- **Modeling**: Implements N-Gram models to predict the next character in a word.
- **Evaluation**: Assesses the model's performance in playing the Hangman game.

## Files
- `hangman.py`: Main Python script containing the implementation of the Hangman game predictor.
- `training.txt`: Text file containing the dataset of words used for training the model.

## Data and Preprocessing
The dataset consists of English words stored in `training.txt`. The words are cleaned and prepared for training the N-Gram models. 

## N-Gram Models
### Unigram
Counts the occurrence of each character in the dataset.

### Bigram
Calculates the probability of a character given the preceding character.

### Trigram
Calculates the probability of a character given the two preceding characters.

### Four-gram
Calculates the probability of a character given the three preceding characters.

## Usage
1. **Clone the repository:**
    ```bash
    git clone https://github.com/yourusername/hangman-game-prediction.git
    cd hangman-game-prediction
    ```

2. **Run the Hangman predictor:**
    ```bash
    python hangman.py
    ```

## Example Code
The following example shows how to use the `suggest_next_letter_sol` function to predict the next letter in a Hangman game.

```python
import string
from collections import defaultdict, Counter
import numpy as np

# Load dataset and define preprocessing steps here

def suggest_next_letter_sol(displayed_word, guessed_letters):
    guessed_letters_set = set(guessed_letters)
    return four_gram_guesser(list(displayed_word), guessed_letters_set)

# Define the four_gram_guesser function and other N-Gram functions here
```

## Results and Discussion
The model's performance is evaluated based on the average number of incorrect guesses. Higher-order N-Grams (e.g., four-grams) provide better context and improve prediction accuracy.

## Conclusion and Future Work
### Conclusion
The N-Gram models, especially the four-gram model, significantly enhance the prediction accuracy in the Hangman game.

### Future Work
- Explore higher-order N-Grams (e.g., five-grams) for more context.
- Implement smoothing techniques for unseen N-Grams.
- Combine predictions from different N-Gram models.
- Investigate neural network approaches (e.g., LSTMs, Transformers) for complex dependencies.

## References
- [Understanding Word N-Grams and N-Gram Probability](https://towardsdatascience.com/understanding-word-n-grams-and-n-gram-probability-in-natural-language-processing-9d9eef0fa058)
- [N-Gram Language Modelling with NLTK](https://www.geeksforgeeks.org/n-gram-language-modelling-with-nltk/)
- [N-Gram Modelling in NLP](https://www.kdnuggets.com/2022/06/ngram-language-modeling-natural-language-processing.html)
- [All About N-Gram Language Models](https://medium.com/ml-purdue/all-about-n-gram-language-models-83c20043b79)

## Authors
- Raj Kanani
- Utkarsh Dubey
- Isha

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```

Feel free to add any more specific links or further details as necessary.
