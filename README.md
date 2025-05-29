# Chess Commentator Transformer

## Overview

This project leverages transformer-based deep learning models to generate human-like commentary for chess games. The project involves mining annotated chess games, preprocessing the data, and training a transformer model to generate move-by-move commentary, aiming to bridge the gap between chess engines and human explanations.

## Video Walkthrough

[![Chess Commentator Transformer Demo](https://img.youtube.com/vi/TRrfl2bLbKY/0.jpg)](https://www.youtube.com/watch?v=TRrfl2bLbKY)

## Project Structure

- `1.Intro.ipynb`: Project introduction, goals, and initial data exploration.
- `2.Data_Mining.ipynb`: Scripts and documentation for scraping annotated chess games from GameKnot.
- `3.Data_Quality.ipynb`: Analyzing the quality of the data, and eliminating outliers.
- `4.Tokenization.ipynb`: Creating custom tokenizers for the encoder and the decoder.
- `5.Training.ipynb`: Details the process of training the transformer model on the prepared dataset.
- `6.Post_Analysis.ipynb`: Comparing train and validation loss accross different models.

## More Information

- `misc/ChessCommentatorTransformer_KazanKerem_Report.docx.pdf`: Full project report.
- `misc/slides.pptx`: Project presentation slides.

## Data Collection & Mining

- **Source**: Annotated games are scraped from the GameKnot website, focusing on games with human commentary.
- **Process**:
  - Scrape game links and extract FEN positions, moves (UCI format), and human commentary for each move.
  - Store the dataset as a CSV file with columns for FEN, move, and commentary.
- **Tools**: `bs4` and `selenium`.

## Data Preparation

- Train custom tokenizers for both the encoder (chess positions/moves) and decoder (commentary text).
- Prepare the dataset for sequence-to-sequence learning.

## Model Training

- **Framework**: HuggingFace `transformers` library.
- **Environment**: Google Colab, with model checkpoints and tokenizers saved to Google Drive.
- **Workflow**:
  - Load and preprocess the dataset.
  - Visualize chess positions and moves.
  - Train a transformer model to generate commentary given a chess position and move.

## Usage

- Run the notebooks 1-4 to completion. You will have a complete dataset and tokenizers.
- Upload `5.Training.ipynb` to Google Colab and run it to train the model.
- Make sure you push your tokenizers and dataset to Google Drive, where you can access them in the next notebook.
- Here's a training run on an A100 on Google Colab: https://colab.research.google.com/drive/1tCtRpZRnNv6Ta6qG9ZFcOab-E2_0NbpW?usp=sharing

## Author

Kerem Kazan

---
