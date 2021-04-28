# db-final-project - Betting-Database
By Sarthak Shrivastava, Zain Alam, Ayan Chowdhury 

NOTE: We are currently attempting to implement linking between our domain and user classes, but at the moment the code reflected does not support that functionality due to trouble on our end. To see the front end for each class, go to the final_project folder. There are three folders, one for each of our implemented classes that have their own index.html file. Run the demo application file and then the index.html in each folder should work. 

This project is a small scale implementation of NBA statistics so that there can be a centralized application where Users can track the progress of their favorite teams and players 
throughout the season. Our database allows users to create an account and make a list of their favorite teams and players, so that they can view the information that is relevant 
to them. We also added statistics about spread and favored teams to our database for those users that are interested in sports betting. 

UML Class Diagram

Users:
Users have a first_name, last_name, username, password, and date_of_birth. It contains the basic characteristics required for all users to have.

Player: 
Players have a first_name, last_name, jersey_number, and team. It represents an NBA player and stores relevant information about their first and last names, as well as a foreign 
key to an entry in the 'Team' table that links these two tables.

Game:
Games have a location, team_one_points, team_two_points, favorite_team, spread, and status. Location is a foreign key to a table that stores matchup data, team_one_points and 
team_two_points represent the score of the game, the favorite_team and spread are betting statistics that are stored for each game, and status is an enum that indicates if a game is 
currently being played, has been played, or is upcoming.

Each user can favorite certain players and teams, and as there may be overlap between users and their favorite teams and players, these are many to many relationships between the 
two tables. The Team table and the Game Table are linked via a Matchup and Location table, as there are two teams per game, but each team has many games that they play in during 
the NBA season. 

The portable enumeration we used was in the Game table and as stated above, it was used to indicate the status of a game: whether it had been played, was currently being played,
or is an upcoming matchup. 

For the user interface, we need to focus on developing a UI for the user class that can allow for CRUD implementations, as well as one for Players, and lastly Games. We also have 
to understand how to link between these tables and develop entry form components and list components for each. 

