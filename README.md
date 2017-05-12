# Movie
Automated API tests for themoviedb.org 

It is recommended that the user executes test scripts from the Postman UI so that inline comments and test details can be viewed.

Running the tests from the Postman UI (recommended):

   1) Download Postman - https://www.getpostman.com/
   2) Select the Import button on the top left
   3) On the pop-up modal, select the 'Import From Link' tab
   4) Paste the following link and click 'Import'
   
https://www.getpostman.com/collections/d8e08d0f0e4c3a1c555a
   
   5) Run the collection tests.  
      a) Click the arrow next to the 'Movie DB' collection
      b) Click the blue 'Run' button (This will open the collection runner)
      c) Enter the number of iterations you would like to repeat the tests (default is 1)
      d) If you enter more than one iteration on step 'e', you can also add a delay between executions
      e) Click the blue 'Start Test' button
      
Running the tests from the command line:

   1) You'll need Node.js installed.  To see if you already do, use 'node -v'
      You can install node here - https://nodejs.org/en/download/
   2) Install Newman - 'npm install -g newman'
   3) 'newman run https://www.getpostman.com/collections/d8e08d0f0e4c3a1c555a'
   
Future enhancements will modify requests to operate using a dedicated 'movie' environment. (Tests were not written this way since sharing environments is only an option in Postman Pro. Manually sharing environments (without Pro) is a bit of a chore.)
