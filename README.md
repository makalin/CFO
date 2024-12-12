# BASIC Game: Catch the Falling Objects

This is a simple game written in QBASIC/QuickBASIC where you control a character ('O') that moves left and right to catch falling objects ('*'). The game demonstrates basic programming concepts such as player input, game loops, collision detection, score tracking, and screen updating.

## How to Play

- Use the 'a' key to move your character left.
- Use the 'd' key to move your character right.
- Catch the falling asterisks ('*') with your 'O' character to increase your score.
- The game runs in an infinite loop until you stop the program.

## Code

### Full Version

```basic
10 CLS
20 X = 40: Y = 22: SCORE = 0: FX = INT(RND * 80): FY = 1
30 LOCATE Y, X: PRINT "O";
40 LOCATE FY, FX: PRINT "*";
50 K$ = INKEY$
60 IF K$ = "a" AND X > 1 THEN X = X - 1
70 IF K$ = "d" AND X < 80 THEN X = X + 1
80 FY = FY + 1
90 IF FY = Y THEN
100   IF ABS(FX - X) <= 1 THEN SCORE = SCORE + 1
110   FY = 1: FX = INT(RND * 80)
120 END IF
130 LOCATE 1, 1: PRINT "Score: "; SCORE
140 CLS
150 GOTO 30
```

### Minimal Version

```basic
10 CLS:X=40:Y=22:S=0:F=RND*80:G=1
20 LOCATE Y,X:PRINT"O":LOCATE G,F:PRINT"*"
30 K$=INKEY$:IF K$="a"THEN X=X-1
40 G=G+1:IF G=Y THEN S=S+ABS(F-X<2):G=1:F=RND*80
50 GOTO 20
```

## Requirements

To run this game, you need a QBASIC/QuickBASIC interpreter. You can use DOSBox to emulate a DOS environment if you're running a modern operating system.

## Installation

1. Download and install [DOSBox](https://www.dosbox.com/).
2. Obtain a copy of QBASIC or QuickBASIC.
3. Create a new file with a `.bas` extension and copy the code into it.
4. Use DOSBox to navigate to the directory containing your `.bas` file.
5. Run QBASIC and load your game file to start playing.

## License

This project is open-source and available under the MIT License. Feel free to modify and distribute it as you wish.

## Contributing

If you have any suggestions or improvements, feel free to open an issue or submit a pull request.

---

Enjoy the game and happy coding!
