# NoSQL Data Analysis using Pymongo, and Pandas

Description: The UK Food Standards Agency evaluates various establishments across the United Kingdom, 
and gives them a food hygiene rating. 
This project evaluates some of the ratings data in order to help their journalists and 
food critics decide where to focus future articles.

First, the "uk_food" database needs to be set up in mongoDB shell.
You can find the installation instructions for this below:
https://www.mongodb.com/docs/mongodb-shell/install/


Instructions for setting up Jupyter Notebook, and mongosh:

        1. Ensure you have downloaded and installed Jupyter notebook via the python index.

        If not, you can find information on how to do this at:
        https://jupyter.org/install
        
        2. Download the NoSQL_setup_starter file & NoSQL_analysis_starter file and 
        the Resources folder into your local directory.

        3. Navigate into this directory from your terminal.

        4. Open Jupyter Notebook in this location. 
        
        5. Open the first file called 'NoSQL_setup_starter.ipynb' into your open notebook.

        6. At the top of this file, you will see the code you need to copy into Terminal. 
        Copy everything *after* the *$* symbol.
        Note- ensure you've followed the instructions at the start of this ReadMe to install mongosh.
        
        7. In your Terminal, navigate into the Resources folder you just downloaded above.
        Paste the copied text into the Terminal. Press Enter.
        
        If your database has been set up properly, you should get a message to say:
        "39779 document(s) imported successfully. 0 document(s) failed to import."
        If not, please return to the mongoDB shell instructions on the website 
        above to seek further instructions or clarity.

        8. Go back to the 'NoSQL_setup_starter.ipynb'notebook and start running each cell.
        
        As you run each cell, you will have set up the establishments collection, 
        within the uk_food database, to start your analysis in the next file.
        A new restaurant called 'Penang Flavours' is also added to the collection.

        9. You are now ready to load the 'NoSQL_analysis_starter.ipynb' notebook.
        In this notebook, please run each cell to get the output you require.

RatingValue refers to the overall rating decided by the Food Authority and ranges from 1-5. 
The higher the value, the better the rating.

Note: This field also includes non-numeric values such as 'Pass', 
where 'Pass' means that the establishment passed their inspection but isn't given a number rating.
The non-numeric values have been coerced to nulls during the database setup before converting ratings to integers.

The scores for Hygiene, Structural, and ConfidenceInManagement work in reverse.
This means, the higher the value, the worse the establishment is in these areas.

The analysis file will give you the following output:

        1. count_documents is used to display the number of documents contained in the result.

        2. The first document in the results is displayed using pprint.

        3. The results are converted to a Pandas DataFrame,the number of rows in the DataFrame are printed,
        and the first 10 rows are displayed.

        4. Establishments are queried that have a hygiene score equal to 20.

        5. Establishments in London are queried that have a RatingValue greater than or equal to 4.

        6. The top 5 establishments with a RatingValue of 5, are queried,
        sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?

        7. How many establishments in each Local Authority area have a hygiene score of 0? 
        Sort the results from highest to lowest, and print out the top ten local authority areas.


Disclaimer- the code for geocoding nearest to Penang Flavours was provided by Mark, a learning assistant from AskBCS.