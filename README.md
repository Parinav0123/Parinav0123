from flask import Flask, render_template, request
from bot import chatbot  # Import the trained chatbot instance

app = Flask(__name__)

# Define a route for the homepage
@app.route("/")
def home():
    return render_template("index.html")

# Define a route for the chatbot response
@app.route("/get")
def get_bot_response():
    userText = request.args.get('msg')
    return str(chatbot.get_response(userText))

if __name__ == "__main__":
    app.run(debug=True)
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Parinav0123/Parinav0123 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
