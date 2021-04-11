# MarsRover kata in Kotlin

## Instructions

You’re part of the team that explores Mars by sending remotely controlled vehicles to the surface of the planet. Develop an API that translates the commands sent from earth to instructions that are understood by the rover.

### Requirements

* You are given the initial starting **coordinate** (x,y) of a rover and the **direction** (`N`, `S`, `E`, `W`) it is facing. (0, 0, N)
* (0,0) are (X,Y) **coordinates** on a planet of (10,10).
* (0,0) is at the bottom-left of the planet.
* The rover receives a character array of **commands** (`RFFLF`) and returns the finishing **coordinate** after the moves (`2:1:N`).
* `L` and `R` allow the rover to rotate to left and right.
* `F` and `B` allow the rover to move forward and backward one point in the current direction.
* The rover wraps around if it reaches the end of the planet.
* The planete may have **obstacles**. If a given sequence of commands encounters an obstacle, the rover moves to the last possible **coordinate**, aborts the sequence and reports the obstacle (`O:2:2:N`).

### Exemples

- given a planet of (10,10) with no obstacles, input `FFRFFLF` gives output `2:3:N`.
- given a planet of (10,10) with no obstacles, input `FFFFFFFFFF` gives output 0:0:N (due to wrap-around).
- given a planet of (10,10) with an obstacle at `(0,3)`, input `FFFF` gives output `O:0:2:N`.
