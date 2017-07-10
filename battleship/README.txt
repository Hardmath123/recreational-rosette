Solve the [Battleship](http://www.conceptispuzzles.com/index.aspx?uri=puzzle/battleships/techniques) puzzle using Rosette.

This a constraint programming exercise and the puzzle has been initialized to [this](http://inst.eecs.berkeley.edu/~rohin/puzzles/battleship.pdf). The approach used here is as suggest by the December 2006 paper [Constraint programming models for solitaire battleships](https://www.researchgate.net/publication/228789470_Constraint_programming_models_for_solitaire_battleships). Do note that the paper does contain a bug[1], as is pointed out by the implementation. Have fun!

[1] Correction in section 2 of Constraint Programming Models for Solitaire Battleships:
In the second paragraph of page 4 which mentions the constraint ensuring correct value of t_{ij}, the constraint should change from:

t_{ij} = max(\sum_k r_{ijk} + \sum_k l_{ijk}, \sum_k u_{ijk} + \sum_k d_{ijk})

to

t_{ij} = max(\sum_k r_{ijk} + \sum_k l_{ijk}, \sum_k u_{ijk} + \sum_k d_{ijk}) + s_{ij}

Note that when t_{ij} is >= 1, the incorrect constraint yields value one less than the actual value and the value of s_{ij} needs to be added to fix that.
