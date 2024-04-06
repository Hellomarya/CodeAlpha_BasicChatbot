# CodeAlpha_BasicChatbot
Task 3 Basic Chatbot
import nltk
import random

# Download NLTK data if not already downloaded
nltk.download('punkt')

# Define responses
responses = {
    "hi": ["Hello!", "Hi there!", "Hey!"],
    "how are you": ["I'm good, thanks!", "I'm doing well, how about you?", "All good here!"],
    "bye": ["Goodbye!", "See you later!", "Bye! Have a great day!"]
}

# Function to get a response based on user input
def get_response(message):
    message = message.lower()
    if message in responses:
        return random.choice(responses[message])
    else:
        return "I'm not sure how to respond to that."

# Main loop for chatting
print("Chatbot: Hello! How can I help you?")
while True:
    user_input = input("You: ")
    if user_input.lower() == 'exit':
        print("Chatbot: Goodbye!")
        break
    response = get_response(user_input)
    print("Chatbot:", response)
