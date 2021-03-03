# 3-Style-Calculator 
Welcome to my 3-Style Calculator. 3-Style is a way of blind-solving the Rubik's Cube; it is the fastest possible method. Unlike Old Pochman and M2, which solves 1 piece at a time, the 3-Style method solves two pieces at once using commutators. Commutators work like this: 
[A, B] = A B A' B' 

Or, if you would like to see it with actual algorithm notation: 
[R U R', D] = R U R' D R U' R' D' 

The key thing to remember is that when performing the inverse of A (or B), you flip the signs of all moves (normal moves like F to F', and vice versa), and you reverse the order in which you performed them (meaning you perform A' from right to left). So, if A = R U R', A' = R U' R'. Here, I reversed the moves R' U R, and flipped the sign of each one (R U' R'). 

What makes 3-Style so difficult is that it has a bunch of cases. There are 441 cases for the edges alone. And there are hundreds more for the corners. 

I got this idea from watching one of JPerm's videos on 3-Style on Youtube. He said that if you were serious about learning this method, try to figure out the commutator by yourself first, as they are mostly intuitive. And then, if you are struggling, you can look at the answer. The problem with that is that the answer is in a 21x21 excel grid, and it can be very difficult to find each case, and execute it correctly. 

So, having all of this information, I went out to build a program that can calculate the commutator from the grid when only given two inputs, the first and second targets. The buffer position is the UF edge piece (which is C in the Speffz Lettering Scheme). Let's say that in that position, you have the letter H; and then, in H, you have P. All you have to do is insert H as the first target, P as the second target, and hit Generate Cycle. This will give you the cycle that you need to do to solve both pieces (H and P) at the same time. I created this program for both edges and corners, so hopefully it helps. 

YOU MUST KNOW THEH SPEFFZ LETTERING SCHEME BEFORE YOU USE THIS PROGRAM. I modeled the code on this scheme, with E as the LU edge piece, and so on. 
