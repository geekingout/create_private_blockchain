# create_private_blockchain

Project intro

Project Introduction
You are starting your journey as a Blockchain Developer. This project allows you to demonstrate that you are familiarized with the fundamental concepts of a Blockchain platform. Concepts like:
- Block
- Blockchain
- Wallet
- Blockchain Identity
- Proof of Existence
- Digital Assets
Are some of the most important components in the Blockchain Framework that you will need to describe and also, why not? Implement too.
In this project you will have a boilerplate code with a REST Api already setup to expose some of the functionalities you will implement in your private blockchain.
What problem will you solve implementing this private Blockchain application?
Your employer is trying to make a proof of concept on how a Blockchain application can be implemented in his company.
He is an astronomy fan and because of that he spends most of his free time searching stars in the sky, that's why he wants to create a test application that allows him and his friends to register stars, and track the ownership of each.
What steps are needed to implement your employers application?
1. The application will create a Genesis Block when we run the application.
2. The user will request the application to send a message to be signed using a Wallet and in this way verify the ownership over the wallet address. The message format will be:  <WALLET_ADRESS>:${new Date().getTime().toString().slice(0,-3)}:starRegistry;
￼
3. Once the user has the message they can use a Wallet (Electrum or Bitcoin Core for example) to sign the message.
4. The user will try to submit the Star object for that. The submission will consist of: wallet address, message, signature and the star object with the star information. The Start information will be formed in this format:     "star": {
￼
5.          "dec": "68° 52' 56.9",
6.          "ra": "16h 29m 1.0s",
7.          "story": "Testing the story 4"
8.      }
9. 
10. The application will verify if the time elapsed from the request ownership (the time is contained in the message) and the time when you submit the star is less than 5 minutes.
11. If everything is okay the star information will be stored in the block and added to the chain encoding the Star information.
12. The application will allow us to retrieve the Star objects belong to an owner (wallet address). This information should be human readable so it shouldn't be encoded.

Project Requirements


Your project will be evaluated using the Project Rubric. For a project to pass, all criteria must Meet Specifications. Please thoroughly read through the rubric before beginning to build your project.
What tools or technologies will you use to create this application?
* This application will be created using Node.js and Javascript programming language. The architecture will use ES6 classes because it will help us to organize the code and facilitate the maintenance of the code.
* We suggest you use Visual Studio Code as an IDE because it will help easily debug your code, but you can choose any code editor you feel comfortable with.
* Some of the libraries or npm modules you will use are:
    * "bitcoinjs-lib": "^4.0.3",
    * "bitcoinjs-message": "^2.0.0",
    * "body-parser": "^1.18.3",
    * "crypto-js": "^3.1.9-1",
    * "express": "^4.16.4",
    * "hex2ascii": "0.0.3",
    * "morgan": "^1.9.1"
Remember if you think you need install any other library you will use npm install <npm_module_name>
Libraries purpose:
1. bitcoinjs-lib and bitcoinjs-message will help us verify wallet address ownership and signatures. Note: Make sure to always use Legacy Wallet addresses.
2. express is a node framework used to create The REST Api used in this project
3. body-parser is used as a middleware module for Express and will help us to read the json data submitted in a POST request.
4. crypto-js is a module containing some of the most important cryptographic methods and will help us create the block hash.
5. hex2ascii will help us decode the data saved in the body of a Block.
Remember all this libraries can be found in the package.json file in your project folder.
