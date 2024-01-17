# chat-web
## How to start.
Hello and welcome to my chat website, first download the zip, unzip it.
<br>
After unziping the folder open the project in vsc, you will need to have vsc, node, mongodb already downloaded to your computer.
<br>
Enter the server directory, in your command line and write npm install to install all the dependencis, 
Make sure that you have installed all required dependencies: npm i express cors body-parser mongoose custom-env socket.io.
<br>
After that, go to the babble diirectory and do the same.
<br>
Open your mongodb server on your computer through mongodbcompass application.
<br>
Go back to the server directory and write nodemon app.js, open your browser to the adress: http://localhost:5001/ ,and start chatting!

## API Functionality

The Babble website incorporates the following API endpoints and functionalities:

* **User**:
  - `GET /api/Users/:username`: Retrieve user details by providing the username.
  - `POST /api/Users`: Create a new user.
  - `PUT /api/Users/:username`: Change displayName or profilePicture for a specific user.

* **Token**:
  - `POST /api/Tokens`: Generate a JSON Web Token (JWT) for registered users.

* **Chats**:
  - `GET /api/Chats`: Retrieve the list of chats for the user.
  - `POST /api/Chats`: Create a new chat.
  - `GET /api/Chats:/id`: Retrieve a specific chat associated with the user.
  - `DELETE /api/Chats/:id`: Delete a chat with a specific user.

* **Messages**:
  - `GET /api/Chats/:id/Messages`: Retrieve the list of messages in a specific chat.
  - `POST /api/Chats/:id/Messages`: Send a message in a specific chat.
  - `GET /api/Chats/:id/Messages/FilesAttach`: Retrieve all file attachments from a specific chat.
  - `GET /api/Chats/Messages/FilesAttach/:msgId`: Retrieve the data of the file attached to a specific message.
<br>
## Notes about Real-Time chatting.
In this project, we have chosen to store the user's information in the localStorage of the browser. This decision was made to ensure that users do not get logged out when they refresh the page or reopen the browser. By utilizing localStorage, we provide a seamless experience where users can continue their session without interruption.

However, it is important to note that localStorage is shared across all tabs within the same browser. While this approach enables persistence, it poses a limitation for experiencing real-time chatting. To fully utilize the real-time chatting functionality, it is required to connect to multiple users using different browsers, or opening a single incognito tab alongside a single regular tab.

