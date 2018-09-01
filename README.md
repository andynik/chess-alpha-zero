# About
Here you can find some code<sup>[[1]](#myfootnote1)</sup> about implementation of chess engine via reinforcement learning of [AlphaZero methods](https://arxiv.org/pdf/1712.01815.pdf).

## Supervised Learning
Supervised learning could be done over PGN games files of professional chess players (with high elo rating that means). This data was taken from the chess database called [FICS](http://ficsgames.org/download.html).

Here some nice results (over 3000 games of SL, elo >= 2000). I'm (white) playing against the program (black):

![I am vs program](https://github.com/andynik/deep-move/blob/master/images/ApronusDiagram1529753143.gif)

To start SL put PGN files in `data/play_data` dir and run the command:

```
python src/chess_zero/run.py sl
```

## Reinforcement Learning
For reinforcement learning use: `self`, `opt` and `eval` commands:

Command | Description
--- | ---
`self` | is Self-Play to generate training data by self-play using BestModel
`opt` | is Trainer to train model and generate next-generation models
`eval` | is Evaluator to evaluate whether the next-generation model is better than BestModel. If better, replace BestModel

All in all it's just about generating PGN data which contains self-played games by the chess engine.

## GUI
You can also run the engine in GUI. To set it up, just point it to `uci.bat` throught GUI environment.

![Running the engine in Arena](https://github.com/andynik/deep-move/blob/master/images/Arena.png)


To find more about the work check out my thesis [over here](https://drive.google.com/file/d/116uMDNDGFkpX7DirNJyG5QGh-QthFG_E/view?usp=sharing)<sup>ua</sup>.


---
<a name="myfootnote1"><sup>1</sup></a> Was forked from [@Zeta36](https://github.com/Zeta36)'s [project](https://github.com/Zeta36/chess-alpha-zero).
