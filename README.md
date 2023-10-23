# Youtube AI Assistant
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This project is built for the purpose of getting summarized text specifically for long-duration YouTube videos and 
also to chat with an AI assistant to get instant answers to your queries related to that YouTube video.<br>
If we stumble upon an interesting video, it's usually not possible to watch the entire video due to time constraints. 
Hence, we can use this app to get summarized knowledge about that specific video.

This project is hosted on HuggingFace Spaces: [Live Demo of Youtube AI Assistant](https://huggingface.co/spaces/heliosbrahma/ai-youtube-assistant).

## Steps:-
- Extract transcript from video using Langchain's YoutubeLoader and then split it into chunks of text using RecursiveCharacterTextSplitter
- Upload chunks of text into Qdrant Vector DB
- Generate summarized text using Langchain's load_summarize_chain
- Retrieve the top 3 similar chunks for each user query using RetrievalQA and using a custom prompt by PromptTemplate, answer those queries

## How to run it locally:-
If you want to run this app locally, first clone this repo using `git clone`.<br><br>
Now, install all libraries by running the following command in the terminal:<br>
```python
pip install -r requirements.txt
```
  
Now, run the app from the terminal:  
```python
gradio app.py
```

_If you like this project, please ⭐ this repository._
