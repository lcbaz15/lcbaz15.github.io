---
layout: post
title:  "Working Together"
date:   2017-07-01 18:51:38 +0000
---


For this lesson, I worked through most of it with another learn student through the chat box. 


I'll use this post to document the problems and solutions posted on the chat. I'll also add my some of my thoughts, in retrospect. 

**
How to use exisiting methods and their inverses:**

cris1314 a month ago
but that method return an array or a false

cris1314 a month ago
and we need a true or false

cris1314 a month ago
so maybe if we just copy and paste the block of code

cris1314 a month ago
and change the return array for return bool

cris1314 a month ago
should work

lcbaz15 a month ago
yeah that makes sense

cris1314 a month ago
nope

cris1314 a month ago
did you have any success?

lcbaz15 a month ago
yeah one sec

lcbaz15 a month ago
`def draw?(board) if !won?(board) && full?(board) return true elsif !won?(board) && !full?(board) return false elsif won?(board) return false end end`

lcbaz15 a month ago
kind of confusing

lcbaz15 a month ago
but that works

lcbaz15 a month ago
i folowed the text word for two elsif statements

lcbaz15 a month ago
one if statement



*I think inverses of methods are so useful, even though they can be confusing to read. They are so efficient!*



**
Matching the indexes of the #board with #won**


cris1314 a month ago
also I have an erro

cris1314 a month ago
returns false for a won game diagonaly

lcbaz15 a month ago
hmmm

cris1314 a month ago
but I'm checking my constant and have the diagonal combination

lcbaz15 a month ago
ok

cris1314 a month ago
do have that error?

lcbaz15 a month ago
no i dont

lcbaz15 a month ago
hmm

cris1314 a month ago
my diagonal combinations are

cris1314 a month ago
[0,4,8], # diagonal1 row [2,4,6], # diagonal2 row

lcbaz15 a month ago
maybe something is wrong with the full? method

lcbaz15 a month ago
because im pretty sure we have the same won? method

cris1314 a month ago
def full?(board) return !board.any?{|i| i == " "} end

cris1314 a month ago
this is my full method

cris1314 a month ago
do you have the same ?

lcbaz15 a month ago
ah thats the issue maybe

lcbaz15 a month ago
def full?(board) board.any? do |index| " " || "" || false end return !board.any?{|i| i == " "} end

cris1314 a month ago
nope

cris1314 a month ago
I have the same error

cris1314 a month ago
ok I did something wrong xD

cris1314 a month ago
the worst part of coding is get stuck jajaja

lcbaz15 a month ago
oh wait!

lcbaz15 a month ago
the second diagonal should be [6, 4, 2}

lcbaz15 a month ago
]*

lcbaz15 a month ago
just need to switch the 2 and 6

cris1314 a month ago
nothing T_T

lcbaz15 a month ago
nooooo -_-

cris1314 a month ago
let me send yo my script xD

cris1314 a month ago
file not allowed to send xD

lcbaz15 a month ago
i can send you a screenshot of what i have!

cris1314 a month ago
please T_T


cris1314 a month ago
I have the same!

cris1314 a month ago
and give me this

cris1314 a month ago
returns an array of matching indexes for a left diagonal win

cris1314 a month ago
returns an array of matching indexes for a right diagonal win

cris1314 a month ago
is the same T_T

cris1314 a month ago
ok!

cris1314 a month ago
I go it

cris1314 a month ago
I don't know why

cris1314 a month ago
but just changing the diagonal values from bottom to the top

cris1314 a month ago
solve the problem

cris1314 a month ago
inside the constant


*This error seemed really random to me, and I'm still not entirely sure why switching the order of the first and last indexes actually works. *

**Getting to the end: Using first index to state winner of game**

cris1314 a month ago
did you finish the winner ?

lcbaz15 a month ago
no still thinking about it

lcbaz15 a month ago
so would it be using the #won method to return the index

lcbaz15 a month ago
and then returning one of the values>

lcbaz15 a month ago
?

cris1314 a month ago
maybe if we use the won? method to know if someone won, then use the array that returns to use all indexes to compare the board values

cris1314 a month ago
if won?(board)

cris1314 a month ago
#code

cris1314 a month ago
else

cris1314 a month ago
return false

cris1314 a month ago
end

cris1314 a month ago
sorry for all messages xD but I think that's the initial structure

lcbaz15 a month ago
yeah

cris1314 a month ago


cris1314 a month ago
but I have only this error

cris1314 a month ago
#winner returns O when O won

lcbaz15 a month ago
yeah same error

lcbaz15 a month ago
youre close

lcbaz15 a month ago
this worked for me

lcbaz15 a month ago
def winner(board) if winner = won?(board) return board[winner[0]] end end



*Maybe instead of calling the first index like that, a more simplified/straight-forward way would be to use the #first method.
*
**The end :)**



