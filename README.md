# translationglossary
This Web App written in Javascript or any different modern programming language help interpreters and translators worldwide to search and find the term with an accuracy of 95% based on the nature of the documents they are translating/interpreting.

To use it, the interpreter login using an e-mail address and a phone number
A security code is sent to the user to be verified or authenticated. After this step, the user is ready to go.

The web app is mainly a glossary. 
1.The basic function helps the user input a term in his native language.
Then the glossary_database_second_language finds him/her a term that is 95% accurate.
The user is given 3~5 options to chose the most accurate one.
The engine understands the context of a natural language or technical language in order to suggest a more accurate term(AI, further development)
2. The advanced function helps the user input a segment or an entire sentence.
Then the glossary_database_second_language finds him/her a term that is 95% accurate.
The user is given 3~5 options to chose the most accurate segment or sentence., 
    otherwise, he can update the glossary.
    once the user's uploads is confirmed to be 100% accurate, it can be added into the main glossary or main database
    this will improve the system as more users gets smarter, the system will also get smarter.
At this level, the brain of our engine understands the context of a natural language or technical language, sentence by sentence, in any context, in order to provide a more accurate term(AI, further development)
    otherwise, it will give a rough suggestion that can be edited by the experienced user or a human who knows the field well.
  

User Interface:
1. has a login page:
       Username, Password, login.
   or register page:
       Username,password, email address, be verified, you're authenticated!
2. has a settings page:
       target language, first language/native language, fields of interpretation with a 5 star rating(the ones  you want the         engine to focus on, in order to help you, for example, you can say
           Medical,
           Law,
           Biology,
           Chemistry,
           Law enforcement,
           Banking,
           Courts,
           Medical Insurance,
           Water management,
           Aerospace engineering,
           Immigration or government services
           Telephone companies
           IT companies,
           etc,etc.)
4. has a text input area that:
    allows him to input a word or sentence in the second/native language,
    then have the results in either
5. has a "switch language button" language A<-switch -> Language B

BACKEND DESIGN:
1. sends all the data the user need to accomplish:
       register
       login
       translate/interpret
2. updates the database to be the most accurate in all the fields, existing and new ones.
3. saves all the data, assign them a rating (1~5 stars, or a % age of accuracy)
4. 

HOW THE SYSTEM WILL EVOLVE:
Any verified/ expert user is allowed to input a new match if the glossary did not yield a result at 95% accuracy. 
All the new input is submitted to the team to be reviewed then approved.
unapproved results should be flagged with "unapproved match" flag and "most popular unaproved match" or give the user a possibility ti improve or explain why the translation is accurate.
Experts will decide , or a jury will decide, or 5 experts from the field will vote on the most accurate to be written as 100% accurate. 

Suggestion from ChatGPT:

Here's a basic outline of how you could structure your web app using HTML, CSS, and JavaScript:

HTML Structure:
index.html: This will contain the structure of your web app, including the login page and the main glossary interface.
html
Copy code
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Glossary Web App</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div id="login-page">
        <h2>Login</h2>
        <input type="email" id="email" placeholder="Email">
        <input type="tel" id="phone" placeholder="Phone">
        <button onclick="sendSecurityCode()">Send Code</button>
    </div>

    <div id="glossary-page" style="display:none;">
        <!-- Glossary Interface -->
    </div>

    <script src="script.js"></script>
</body>
</html>
CSS Styling:
styles.css: Define styles for your web app.
css
Copy code
/* Add your CSS styles here */
JavaScript Functionality:
script.js: Implement the functionality of your web app.
javascript
Copy code
// Function to send security code
function sendSecurityCode() {
    // Validate email and phone inputs
    var email = document.getElementById('email').value;
    var phone = document.getElementById('phone').value;

    // Implement logic to send security code
    // This could involve sending a code to the provided email or phone number
}

// Function to switch language
function switchLanguage() {
    // Implement logic to switch between native and second language
}

// Function to search glossary
function searchGlossary(term) {
    // Implement logic to search the glossary database
    // and return results with 95% accuracy
}

// Function to submit new match
function submitNewMatch() {
    // Implement logic to submit a new match to the team for review
    // This could involve sending the new match data to a server endpoint
}

// Function to handle login and display glossary interface
function handleLogin() {
    // Implement logic to verify user's credentials (email/phone verification)
    // If verified, display the glossary interface
    document.getElementById('login-page').style.display = 'none';
    document.getElementById('glossary-page').style.display = 'block';
}

// Call handleLogin() when the page loads (for testing purposes)
window.onload = handleLogin;
This is just a basic setup to get you started. You'll need to implement the actual functionality for sending security codes, verifying users, searching the glossary, switching languages, and submitting new matches. Additionally, you'll need to handle user authentication, database interactions, and server-side processing for reviewing and approving new matches. You can use frameworks like React, Angular, or Vue.js to build a more structured and scalable application.


