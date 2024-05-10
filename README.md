# Project Name: Book Management
Book Management provide a platform for you to manage your personal library and discover new books.

#### Part 1:
![book1 Demo](/client/public/images/book1.gif)
#### Part 2:
![book2 Demo](/client/public/images/book2.gif)
#### Part 3:
![book3 Demo](/client/public/images/book3.gif)

### Technologies: 

| Backend 	| Frontend 	| Database   	| Testing   	|
|---------	|----------	|------------	|-----------	|
| Node    	| Vite     	| PostgreSQL 	| RTL       	|
| Express 	| React    	| SQL        	| Vitest    	|
| Postman 	|     	    |         	    |       	    |


### Dependencies: 

| Backend      	| Frontend        	| Database 	| Testing                   	|
|--------------	|-----------------	|----------	|---------------------------	|
| cors         	| react-bootstrap 	| pg       	| @testing-library/react    	|
| dotenv       	| bootstrap       	|          	| @testing-library/jest-dom 	|
| concurrently 	| react-router-dom 	|          	| vitest-dom                	|
| nodemon      	|                 	|          	|                           	|
 
## DB SCHEMA
![schema](/client/public/images/schema.png)

## Tests Summary:
1. The `Introduction` component is tested to ensure it renders a welcome message, a platform description, and an `AuthNav` component. The tests use the `render` and `screen` utilities from `@testing-library/react` to render the component and query elements for testing. Each test asserts that the expected elements are rendered in the component, providing basic coverage for the component's rendering behavior.

2. The `MovieCard` component test suite ensures that the component renders a card with the correct title, image, and a link to the book details page. It tests that the `MovieCard` component behaves as expected by verifying that the title and image are rendered correctly and that the link points to the correct book details page based on the provided ID. The tests use React Testing Library to render the component and assert that the expected elements are present and have the correct attributes.

## Step-by-Step Setting up Instructions - To use this project as your starting point  🚀  
### To create the whole project


1. Go to your source directory in your terminal and run the command `https://github.com/zhjiang1103/bookManagement.git NAMENEWDIRECTORY`

2. To clean the owner git out of the main directory, run the command `rm -rf .git`

3. Run the command `git init` to start your own git track 

4. Go to the server folder in the project (`cd server`) and run the command `npm install`

5. Inside your server folder, open the file `.env.example` and copy the correct option for your configuration found there to your new .env file. 

Here is what your `.env` might look like:

```
DATABASE_URL="postgresql://user:password@localhost/database"
openai_key = "...."
MovieDB_API_KEY = "..."

//Config values for Auth0 - 
SECRET=""
BASEURL="http://localhost:3000"
CLIENTID=""
ISSUER=""

//change from DB_URI to DATABASE_URL
``` 

6. Go to the client folder in the project (`cd .. and cd client`) and run the command `npm install --save --legacy-peer-deps`

🔎 The `npm install` command installs the required dependencies defined in the package.json files and generates a node_modules folder with the installed modules.

7. If you want to run both servers concurrently (which is already a npm dependency on the server) you can keep the script in the package.json in the server that reads `"dev": " concurrently 'npm start' 'cd .. && cd client && npm run dev' "`. If you run the command `npm run dev` from within your server, both the client and backend servers will start.

10. Go to localhost:3000  💪

⚡ **Notes** ⚡  
* React requires **Node >= 14.0.0** & **npm >= 5.6**
* Please note that your backend server will run from `port 8080`, and your frontend React server will run from `port 3000`.

⚙️ Links that you could need:

* The instructions for [pg](https://node-postgres.com/apis/pool)  
* Setup [postgres correctly](https://github.com/Techtonica/curriculum/blob/main/databases/installing-postgresql.md)


