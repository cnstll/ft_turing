# ft_turing

## Goal of the project
The goal of this project is to write a program able to simulate a single headed, single
tape Turing machine from a machine description provided in json.
This project is to be written in functionnal. We picked OCaml as advised. 

As stated below, you will be free to use any libraries you like. The project is also a
good opportunity to discover famous and widely used libraries like Core or Batteries
to name a few

## Description of valid config keys

- **name**: The name of the described machine
- **alphabet**: Both input and work alphabet of the machine merged into a single alphabet for simplicity’s sake, including the blank character. Each character of the alphabet must be a string of length strictly equal to 1.
- **blank**: The blank character, must be part of the alphabet, must NOT be part of the input.
- **states**: The exhaustive list of the machine’s states names.
- **initial**: The initial state of the machine, must be part of the states list.
- **finals**: The exhaustive list of the machine’s final states. This list must be a sub-list of the states list.
- **transitions**: A dictionnary of the machine’s transitions indexed by state name. Each transition is a list of dictionnaries, and each dictionnary describes the transition for a given character under the head of the machine. A transition is defined as follows:
  - **read**: The character of the machine’s alphabet on the tape under the machine’s head.
  - **to_state**: The new state of the machine after the transition is done.
  - **write**: The character of the machine’s alphabet to write on the tape before moving the head.
  - **action**: Movement of the head for this transition, either LEFT, or RIGHT.

## References
- [On Turing Machine - Stanford](https://plato.stanford.edu/entries/turing-machine/)
- [Description fo turing machine](https://www.liafa.jussieu.fr/~carton/Enseignement/Complexite/MasterInfo/Cours/turing.html)

## Tools and libraries
- [Core](https://opensource.janestreet.com/core/)
- [Batteries](https://ocaml-batteries-team.github.io/batteries-included/hdoc2/)
