# Project Statement

## Problem Statement

Spam messages are annoying at best and dangerous at worst — fake prize wins, phishing links, "your account has been suspended" type messages designed to trick people into clicking or handing over info. Big platforms already solve this at scale, but I wanted to understand how spam detection actually works instead of just using it as a black box. So the goal here was simple: build a model that can look at a message and decide, on its own, whether it's spam or a normal (ham) message — using an actual ML approach instead of just hardcoding a list of "spammy" keywords.

## Scope of the Project

This is meant to be a learning project, not something you'd deploy in a real inbox. Here's what it actually covers:

- Building a text classifier on a small labeled dataset (100 messages)
- Using Naive Bayes along with a bag-of-words representation (CountVectorizer)
- Training the model, splitting the data, and checking how accurate it is
- Letting you type in your own messages and see the prediction live

What it's **not** trying to do:

- Hook into real email accounts like Gmail or Outlook
- Handle a massive, real-world dataset
- Use anything fancy like deep learning or transformers
- Come with a proper web interface (that's more of a "maybe later" idea)

Basically, it's small on purpose — the point was to actually understand every step of the pipeline, not build something production-ready.

## Target Users

- Students like me who are learning ML/NLP basics and want a project that's simple enough to actually follow end to end
- Anyone who's curious about how spam filters work behind the scenes
- Beginners looking for a small project to practice the full ML workflow — from raw data all the way to a working prediction

## High-Level Features

- Takes in any message and predicts spam or ham
- Uses Multinomial Naive Bayes for the classification
- Converts text into numeric features with CountVectorizer
- Prints out model accuracy after testing on unseen data
- Lets you interactively test messages right from the terminal
- Kept the code simple on purpose, so it's easy to build on later (swap in TF-IDF, try other models, use a bigger dataset, etc.)
