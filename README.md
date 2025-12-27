Solution
Overview

This repository contains a Python implementation for computing the Givens rotation angles required to prepare a quantum state with real amplitudes 
𝑎
,
𝑏
,
𝑐
,
𝑑
a,b,c,d, as described in the QHack 2022 coding challenge.

Given normalized amplitudes, the function calculates three rotation angles 
𝜃
1
,
𝜃
2
,
𝜃
3
θ
1
	​

,θ
2
	​

,θ
3
	​

 that can be used to construct the desired quantum state using a sequence of Givens rotations.

Approach

The solution analytically derives the rotation angles using trigonometric relationships between the amplitudes:

𝜃
2
θ
2
	​

 is computed using the ratio of amplitudes 
𝑐
/
𝑏
c/b

𝜃
3
θ
3
	​

 is computed using the ratio of amplitudes 
𝑑
/
𝑎
d/a

𝜃
1
θ
1
	​

 is computed using the sine relationship involving 
𝜃
2
θ
2
	​


All angles are returned in the correct order and within the ranges specified in the challenge statement.

File Description

solution.py
Contains the implementation of the givens_rotations function and the required input/output interface for automated evaluation.

Usage

The program reads four comma-separated real numbers from standard input representing the amplitudes 
𝑎
,
𝑏
,
𝑐
,
𝑑
a,b,c,d.

Example
echo "0.5,0.5,0.5,0.5" | python3 solution.py

Output
theta_1,theta_2,theta_3


(Printed as comma-separated floating-point values.)

Function Definition
givens_rotations(a, b, c, d)

Parameters

a, b, c, d (float): Normalized real amplitudes of the quantum state.

Returns

list[float]: A list containing [theta_1, theta_2, theta_3].

Dependencies

Python 3

NumPy

Notes

The input amplitudes are assumed to be normalized.

The code follows the exact input/output format required by the QHack evaluation system.

No modification should be made to the __main__ input/output block.



Submitted as part of QHack 2022 – Coding Challenges.
