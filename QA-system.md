### Programming Assignment2 is about creating a interactive question answering using python
As given we have created our QA system such that it will be able to answer "Who, What, When, and Where" type of questions. It aslo handles questions from any domain.
we have followed AskMSR approach and created our own answer patterns
------------------...............-------------------

Our approach aims to prioritize the keywords extracted from the question for generating most relevant answers.   
'''For example: what is natural language processing? Answer : Natural language processing (NLP) is an interdisciplinary sub field of computer science and linguistics. '''    


we were able to match most of our answer patterns and also we tried to construct answers from partial information such that is was able to recognize the question and respond appropriately and if cannot recgonize the question it responds as "please give me a valid question"    
'''For example: 1.where is charminar/ Answer : Please provide a valid search query    

2.who discovered india? Answer : Ambiguous search query. "Also it gives the possible search options it was able to find." '''      

Finally when user says "exit" it exiits the program by Thank you ! Good bye.       


***LET US LOOK AT OUR ALGORITHM:***     
Step 1: The algorithm takes a question as its input.   
Step 2: Then Analyzes the question based on it type (first word)    
Step 3: It extracts the keywords from the question,then it combines all the keywords extracted (prioritizing entites and nouns) to form a search query.   
Step 4: Using the search query,it searches the wikipedia to find the information.    
Step 5: Finally, ot retrieves relevant information and returns thr answer respectively.    

Here are the basic techniques used: 1) For processing we used techniques like Tokenization, POS tagging, and Entity Recognition 2) For searching we used Wikipedia library to interact and get information. 3) Finally the interactive loop is used to enter the input and get answer.

The detailed description of code lines are explained at there place respectively.
Finally it is like Input processing -----> Question Type Determination -----> Keyword Extraction ------> Wikipedia Search----> Answer retrieval. '''    
   
References used: 
[1] Github page: https://github.com/norib016/Question_Answering_System_Python/blob/master/qa-system.py by Sree Bhanu nori   
[2] Dr. Liao Code Examples and Video Lectures given on BlackBoard.   