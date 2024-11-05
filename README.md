# ILSUM-FIRE
The third edition of ILSUM consist two tasks,  Task 1: Language Summarization For Indian Languages  Task 2: Detecting Factual Incorrectness in Machine Generated Cross Lingual Summaries

## Official Site - https://ilsum.github.io/ilsum/2024/index.html
## Team Name: Curious Coders
## Results: https://ilsum.github.io/ilsum/2024/Result.html

## Files: https://drive.google.com/drive/folders/1Gx0qADUm6qX_wLk1AK9JDkHagKSBJ-Pj?usp=sharing

## MODELS USED:
### Task-1:
  https://huggingface.co/csebuetnlp/mT5_multilingual_XLSum
### Task-2:
  https://ollama.com/
  
## CHALLENGES FACED:
### Task-1:
	1.Could not find a good model specifically for summarization which could handle all the desired languages.
	2.For kannada -> had to convert to english -> summarize -> back to kannada
	3.Limited Google Colab RunTime (90 mins only, after that disconnects, free version)
	4.No GPU on Local PC (3hrs per epoch on colab's t4 GPU, but 72hrs per epoch on my laptop)
	5.CUDA memory limit exceeded (had to use batch processing with very less batch sizes)
### Task-2:
	1.Could not find direct Summary classification models which can understand hindi/gujarati
	2.Could not find LLMs that can understand hindi/gujarati (that's what I thought till I realised Ollama can understand Indian languages)
	3.Difficulty in training LLM because some of the attributes in trainset like Incorrectness_Type,Incorrect_Summary,Correct_Summary or a combination of these were missing (had to change prompting accordingly)
	4.Sometimes outputs included extra explanation beyond just Incorrectness_Type (because it was an LLM). Removed them manually as the test set was small.
