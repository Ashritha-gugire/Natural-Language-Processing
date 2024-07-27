## Designing a chatbot using python NLP [Programming Assignment 1] 

### Introduction: 
Our chatbot typically is designed to facilitate a conversational interface, particulary for assisting student or prospective students interacting with a bot representing George Mason University. Mr.Bot aims to respond appropriately to various user inputs, guiding them through common queries related to admissions, courses status inquiries and more.

User's input triggers different responses from the bot based on predefined patterns
The dictionary consists of regular expressions as keys and lists of corresponding responses as values.
key is a regular expression which is used for word spotting. Value is the possible answer. If a match has been found by using the regular expression, Eliza Mr.Bot will randomly choose an answer from the dictionary values.

The regular expressions used are:

-(Hello|Hi|Hey) : Matches various forms of greetings from the user.   
-university: Matches user mentions of the term "university".    
-student : Matches queries related to being a student or applying for degrees.    
-(study|course|classes|subject): Matches user queries related to studies.      
-(admission|query|status|documents): Matches queries related to admissions or status.    
-graduate: Matches queries related to graduate studies.     
-undergraduate: Matches queries related to undergraduate studies.     
-(international|citizen) : Matches queries related to international students.    
-want : Matches user expressions of desires or intentions.    
-will : Matches user expressions of plans or intentions.     
-yes/no: Matches user affirmations.      
-(thanks|thank you) : Matches expressions of gratitude from the user.     
others: Default regular expression that matches any input if none of the above patterns match.    

References used: 
***[1] Provided by Professor github.com/norib016/Developing_A_Chatbot_Python/blob/master/eliza.py***
***[2] A blog: Building a simple chatbot***

The purpose of our Assignment was to build a simple successful chatbot, where it can give a 
response when user asks a question (i.e it’s basically a conversation between programmer and 
Chatbot and it is designed in such a way as per the given hints and guidelines by the professor). 
The name given to our chatbot ELIZA is “Mr.Bot”, It can initialize a dialogue and encourage the 
programmer to talk. Eliza plays a role of a UniversityCompanian, she can initialize a dialogue 
and encourage user to ask questions and talk with her. 

The whole project starts with Eliza’s Self introduction, and the question “What is your name?”. 
After this initial step, the user can ask questions or input his/her responses. Mr.Bot tries to 
understand the input by keyword matching. 
 

#### Workflow of the project (including algorithms)  

Initialize a dialogue by Eliza's self-introduction and a question  
ex: I'm your Eliza Mr.Bot. What's your name?     
***Main Chatbot Function (chatbot()):***
The main function of the chatbot script. It initiates the conversation, interacts with the user, and 
handles responses. - The chatbot prompts the user for their name, then enters a loop to continuously receive input from the 
user until the user decides to quit. 
def chatbot(): 
print("Hello! I'm your Eliza Mr.Bot. What's your name?") 
user_name = input("You: ") 
➔ The above function prompts the user for their name. 
while True: 
user_input = input(f"{user_name}: ") 
if user_input.lower() in ['quit', 'bye', 'exit']: 
print("Chatbot: Bye! Have a nice day.") 
break 
➔ While loops checks if the user wants to quit or not  

***Response Handling Function (get_response(user_input)):*** 

-This function processes the user input and returns an appropriate response. - It matches the user input against predefined patterns in a response dictionary and selects a response based on the matched pattern. - If no match is found in the dictionary, it checks for responses in a text file and returns a response if a match is found. 

-If neither the dictionary nor the file contains a matching response, it returns a default response.      

get_response(user_input) Function    
This function is responsible for generating a response based on the user input.     
#### Functionality:     
1. Pattern Matching:      
- The function iterates over each key-value pair in the response_dict dictionary, where each key represents a regular expression pattern, and each value is a list of possible responses.    
- It checks if the user input matches the current pattern using re.match() function. The re.IGNORECASE flag is used to perform a case-insensitive match.    
  
2. Response Selection:   
- If a match is found, the function selects a random response from the corresponding list of responses using random.choice() function.    
  
3. Placeholder Replacement:    
- If the selected response contains a placeholder %, the function replaces it with an appropriate value using the transform_pronouns function.    
- The placeholderindicates where the matched part of the user input should be inserted.   
   
4. Return Response: - The function returns the selected response and exits.    
5. Checking in File: - If no match is found in the response_dict, the function calls the get_response_from_file()    
function to check for responses in a text file. - If a response is found in the file, it returns that response.    
Usage 
To use the chatbot:   
1. Run the script.    
2. Enter your name when prompted. 
3. Start typing your queries or messages.    
4. To quit the chat, type "quit", "bye", or "exit".    
1. Techniques - NLP-related -- word spotting by using regular expressions and re syntax(re.findall and     
re.search). -- string operations, such as "re.sub", "join", "string.rstrip()" -- sentence tokenization -- case convert --Python -- input and print founctions -- dictionary and list -- while and for loop -- if/else logic -- 
%s placeholder -- making beep sound -- random package 
