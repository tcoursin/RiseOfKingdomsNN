# Rise Of Kingdoms Neural Nets
Neural net to scan pictures (trained on the game Rise Of Kingdoms)

This is a project done in preperation of an ingame (in the game ROK) event. 
I was too lazy to write down all these statistics and thus made this.

The main directory has two folders: one for pytesseract and one for my own neural net (NN).
The pyesseract folder is used to scan these images with Google's pretrained NN. This only got around 75% accuracy since it is
not trained on this font I guess.
So I made my own NN, you find this in the "own NN" folder. It has three subdirs for three different parts.
1. ReadPower: It is a NN trained to read digits 0-9 and scans the predetermined area and ouputs the digits found.
This is set up so that it will scan the top 200 in the game, so it needs screenshots from the top 200 leaderboard.
2. ReadNames. This is a NN trained to read all characters (lowercase and uppercase). 
This is set up so that it will scan the top 200 players in the game, so it also needs screenshots from the top 200 leaderboard.
3. ReadStats. This is s program using both the NN trained in the previous parts. It takes in screenshots of the players stats
and outputs all these stats in a csv file.
4. It does exactly the same as ReadPower but then with a videostream instead of manually created screenshots. It does classify them wrong sometimes and therefore adds a few extra powers to overall power.

TODO:
- welp comments are still needed

CREDITS:
 - Abid Rahman K in https://stackoverflow.com/questions/9413216/simple-digit-recognition-ocr-in-opencv-python
