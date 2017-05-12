# Movie
Automated API tests for themoviedb.org 

It is recommended that the user executes test scripts from the Postman UI so that inline comments and test details can be viewed.

<h3>Running the tests from the Postman UI (recommended):</h3>

   1) Download Postman - https://www.getpostman.com/
   2) Select the Import button on the top left
   3) On the pop-up modal, select the 'Import From Link' tab
   4) Paste the following link and click 'Import'
   
    https://www.getpostman.com/collections/d8e08d0f0e4c3a1c555a
   
   5) Run the collection tests
     * Click the arrow next to the 'Movie DB' collection
     * Click the blue 'Run' button (This will open the collection runner)
     * Enter the number of iterations you would like to repeat the tests (default is 1)
     * If you enter more than one iteration on step 'e', you can also add a delay between executions
     * Click the blue 'Start Test' button
      
<h3>Running the tests from the command line:</h3>

   1) You'll need Node.js installed.  To see if you already do, use-
   <code>node -v</code>
      You can install node here- 
    https://nodejs.org/en/download/
   2) Install Newman-
       <code>npm install -g newman</code>
   3) Run the collection-
   <code>newman run https://www.getpostman.com/collections/d8e08d0f0e4c3a1c555a</code>
   
Future enhancements will modify requests to operate using a dedicated 'movie' environment. (Tests were not written this way since sharing environments is only an option in Postman Pro. Manually sharing environments (without Pro) is a bit of a chore.)


<h3>List of test covered:</h3>

<strong>Details based on id</strong>
   - Response time is less than 500ms
   - Status code is 200
   - Response content is in JSON format
   - The IMDB ID is accurate
   - The three production companies are accurate
   - Run time is accurate
   - The three film languages are English, Japanese and French

<strong>Search - Inception</strong>
   - Response time is less than 500ms
   - Status code is 200
   - Response content is in JSON format
   - The title is accurate
   - The language is English
   - The release date is accurate
   
<strong>Search - Arrival</strong>
   - Response time is less than 500ms
   - Status code is 200
   - Response content is in JSON format
   - The title is accurate
   - The language is English
   - The release date is accurate
   
<strong>Failure validation</strong>
   - Response time is less than 500ms
   - Status code is 401
   - Response content is in JSON format
   - The status message is accurate
   - Validate that success = false
   - The status code is 7
