**##TIC-TAC-TOE Game README##**
-
This is tic-tac-toe game realisation on Spring Boot framework with use of Spring jpa, REST controller, in-memory database (h2) for backend and thymeleaf template engine, JQuery for frontend user interface..

**##HOW TO USE##**
-
- Compile to JAR archive
- Browser entry point: http://localhost:8080

**##HOW TO USE##**
-
Project has a RESTfull Apis that are as follows.

- /api/tictactoe/game/newgame (POST)
requires params: "player" - name of player.
Success: creates a new game instance in the DB, returns HttpStatus 200 and json serialisation of this game object.
Failure: returns HttpStatus 400.

- /api/tictactoe/game/{id}/connect (POST)
requires params: "player" - name of player, pathvariable {id} - ID of pending game.
Success: join a specified game instance, returns HttpStatus 200 and json serialisation of this game object.
Failure: returns HttpStatus 400.

- /api/tictactoe/game/{id}/currentstate (GET)
requires params: pathvariable {id} - ID of pending game.
Success: returns HttpStatus 200 and json serialisation of game object specified by ID.
Failure: returns HttpStatus 400.

- /api/tictactoe/game/{id}/getwinner (GET)
requires params: pathvariable {id} - ID of pending game.
Success: returns HttpStatus 200 and json serialisation of player object who won the game (if any), which is specified by id.
Failure: returns HttpStatus 400.

- /api/tictactoe/game/{id}/move (POST)
requires params: pathvariable {id} - ID of pending game, "move" - id of field, "player" name of player.
"move" is a parameter from standart tic-tac field (a1,a2,a3,b1,b2,b3,c1,c2,c3), to which the specified player can move.
Success: returns HttpStatus 200.
Failure: returns HttpStatus 400.

- /api/tictactoe/game/{id}/endgame (POST)
requires params: pathvariable {id} - ID of pending game.
This command ends the specified game without winner calculation (draw).
Success: returns HttpStatus 200.
Failure: returns HttpStatus 400.

**## HOW TO PLAY THE GAME##**

----- PLAYER 1 ------
- launch the app and access the localhost as describe above.
- Enter your name and click 'New Game' button to create a new game (If you have'nt created a game yet)
- Wait for socnd player


----- PLAYER 2 ------
- launch the app and access the localhost as describe above.
- Enter your name and click 'Join' button shown in the middle of the screen to join the game that is waiting for you.
- Game will Start 

-- blue crosses are your's and red circles are of opponents.


ENJOY YOUR GAME