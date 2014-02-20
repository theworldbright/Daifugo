Daifugo======Description-----------
Daifugo is a Japanese card game in which players strategically try to get rid off all the cards in their hands. Players take turns playing cards from their hands while obeying the restrictions set by previously played cards. The winner is the player who is able to get rid off all of his or her cards first. Please read the [manual](manual.pdf) for a more detailed description.Configuration Instructions--------------------------
Perform a default build on the server project and run the jar file as follows (JRE 1.7+ is required):`java -jar server.jar`The application uses ports 23548 ~ 23551 by default. Hitting <i>q</i> will shut down the server application.Modify the HOST constant in ClientMain.java to match the server’s IP address and perform a default build on the client. Distribute the client.jar file. Account details will be stored in an automatically generated file, daifugo.xml, in the server’s root directory.To Play-------
A user who opens the distributed jar file will be greeted with a login screen. There the user can immediately create an account and login to a selected room. When two or more users login to the same room, they can start a game by pressing the start button on the control panel located toward the bottom right.Libraries/Frameworks Used-------------------------
* [netgame.common] (http://math.hws.edu/eck/cs124/javanotes6/index.html)* [Card](http://math.hws.edu/javanotes/source/Card.java), [Hand](http://math.hws.edu/javanotes/source/Hand.java), and [Deck](http://math.hws.edu/javanotes/source/Deck.java) classes* [jdom 2](http://www.jdom.org)Known Bugs/Limitations----------------------
The application was not designed with the intent to be distributed in mass. There is no encryption used for the passwords, and a linear search algorithm is used for querying usernames. Before any new functionality is added, the Validator class needs to be refactored.