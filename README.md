# ELLs-Machine-Learning
By Eric McKevitt
---

In this project, I developed an Automated Essay Evaluator catered to English Language Learners using Long Short-Term Memory (LSTM) neural networks. This system leverages advanced Natural Language Processing (NLP) techniques to grade essays on six key aspects - cohesion, syntax, vocabulary, phraseology, grammar, and conventions.

The project's central element was the development and training of individual LSTM-based machine learning models for each of these aspects. LSTM's ability to retain patterns over time makes it ideal for text-based tasks where sequential/contextual information is key. RandomForestRegressor and Support Vector Regression (SVR) models were also implemented for comparison. The simplicity of these models allowed for extensive hyperparameter tuning and rapid training times. Despite this, LSTMs demonstrated a higher performance ceiling due to their greater complexity and ability to effectively handle sequential data.

Essays were converted into sequences via Keras' Tokenizer and pad_sequences, ensuring effective linguistic and structural analysis.

To improve accessibility, I created a web API using Flask, allowing users to submit essays for grading through a simple POST request. I leveraged ngrok to make the local server internet-accessible, ensuring broader usability. Upon submission, the essay is tokenized, padded, and evaluated by the six trained LSTM models. The resulting scores are converted from a normalized form to a 1-5 scale to mimic traditional grading scales, and are returned in JSON format.

This project highlights AI's transformative potential in education, demonstrating how it can automate complex tasks like essay grading. The comparative study between LSTM, RandomForest, and SVR underlines the superior performance of LSTM neural networks in understanding and evaluating written text. Future work may include exploring alternative neural network architectures, such as transformers, for enhanced performance.
