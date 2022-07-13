# Quiz_app-using-PYgame
Made Quiz app by implementing concepts of PYame, OOP, Exception Handeling and and urllib3 module.
My first code based Project.
It took me around 5 days to build this.


![Screen Shot 07-13-22 at 06 02 PM](https://user-images.githubusercontent.com/100014146/178735622-e78aa352-904b-4583-9a8e-4fcb92b49e27.jpg)

![Screen Shot 07-13-22 at 06 02 PM 002](https://user-images.githubusercontent.com/100014146/178735701-8687081a-7320-4b4e-8941-0af5dec08e94.jpg)


Use the screen_setup.py file to setup your pygame environmnt screen. It has all the necessary classes methods thar are required to make this game.

Here, i have tried to implement the knowledge that i had learnt a day before. That is object oriented programming. i had tried to implement classes and object to make this project a success. the methords like getters and setters are also used to make this project.



The question used in this project has two variations:
1.  Offline database
2.  Online database

Object stored in a List!

![Screen Shot 07-13-22 at 06 03 PM](https://user-images.githubusercontent.com/100014146/178735757-5c0872e6-c8f7-4031-a870-c5316c9995f2.jpg)
![Screen Shot 07-13-22 at 06 03 PM 001 (1)](https://user-images.githubusercontent.com/100014146/178735824-1f6d317c-7fae-402f-bce4-835da8e6906e.jpg)

1.Offline database is used when the internet connection of the user is not available. The questions are stored in the list data_struture as an object of Question class.
this allows us to access the question and the respective answer simply by using
question.text attribute for question and 
question.answer for the answer,
where question being the object of the Question class.

Trivia Api used to get realtime dataset
2.Online database: Offline database was the initial database i used to build the entire database. But to level up the project i had used Trivia Database. It is an Api this delivers list of questions according to the category, level of difficulty and type of question. Trivia Api delivers question in Json format.

Now, to get questions from the Json we use urlib3 Package in python. which gets us the data in form of a dictionary.

But, as we converted html to a text dictionary there are few tags like &quot; in the dataset.
thus we use data preprocessing to clean this abnormalties in the dataset. To do this we use python replace function to replace it with corresponding symbol.



Nowthe problem with displaying question onthe sreen is limited area to display on screen. that is whenever we try to print question on screen, it gets printed on a single line. But the width of thedisplay area is fixed (that is 211px in my screen), 

thus to fix this  we use Python's text Wrapper function to splite the question after specific number of characters. this stores the question in prarts in a list and we print it according to the length of the list.


Now the reason to use two databases that is offline and online is whenever the internet is down of the user, the urlib3 tries to make a contact with the trivia Api link , but as it fails Runtime error is thrown. 
To fix this we use Exception handelling concepts in java. so basically we use try -except methord to solve this issue. we place online database in the  try block and offline database in the except block. thus whenever such exception occure the programing automatically shifts to the offline database and carries out further process.





Finally to make this program super intersting and convinient, i had created an .exe file of the game using Pyinstaller module.
here the catch is when we try to create single .exe file of the game, it takes time both for creating .exe file and and ruunning it. thus to fix this we create a pre-extracted folder out of thegame  and archieve it using inno game setup creator to make a sigle .exe file that we use to install ay other game.

command to create pyinstaller game dependency files
    Type in the Cmd at the locationof the game files
    pyinstaller -w starting_file_name.py
    
here we use the files present in the dist folder of the code




