# Youtube AI Assistant
In this project, transcript is being extracted from youtube video and then we get summarized text from extracted transcript.
We can also interact with the chat interface to get instant answers for queries related to the youtube video.

This project is hosted on HuggingFace Spaces: [Live Demo of Youtube AI Assistant](https://huggingface.co/spaces/heliosbrahma/ai-youtube-assistant).

## Steps:-
- Extract transcript from video using Langchain's YoutubeLoader and then split it into chunks of text using RecursiveCharacterTextSplitter
- Upload chunks of text into Qdrant Vector DB
- Generate summarized text using Langchain's load_summarize_chain
- Retrieve top 3 similar chunks for each user query using RetrievalQA and using custom prompt by PromptTemplate, answer those queries

## How to run it locally:-
If you want to run this app locally, first clone this repo using `git clone`.<br><br>
Now, install all libraries by running the following command in terminal:<br>
```python
pip install -r requirements.txt
```
<br><br>
Now, run the app from terminal:<br>
```python
gradio app.py
```
