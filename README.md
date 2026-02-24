These files contain the computational labour of my Master's thesis. I have implemented a method of Bright and Siksek in [BS08], 
that is useful for proving a given n-covering of an elliptic curve is an element the Tate-Shafarevich group. We implement 
two primary cases: (1) 2-coverings of elliptic curves and (2) one special 3-covering example known as Selmer's curve.
For (1), the code we write is much more generalised and should (theoretically) work on any 2-covering. There will always be
exceptions, and I imagine if you run the code for long enough it will eventually break. However, it is verified to function
for various examples. You find this in the files ... 

For (2), we examine the special cubic 3X³ + 4Y³ + 5Z³ = 0, known for violating the Hasse principle. You find the contents of these 
computations in Selmer Curve.mag and Eisenstein Integers.mag. The Latter file contains the methods for factorising integers in 
Z[rho] for rho^2 + rho + 1 = 0. It also contains a function for computing the gcd of two Eisenstein integers. The first file, is 
the more interesting one, and it contains the computations that are the primary subject matter of [BS08]. The code is NOT automated:
it requires careful analysis to actually use. In any case, one should be able to replicate the computations performed. We must compute
local Hilbert symbols in these computations, and do this we use the algorithms of https://github.com/kodebro/powerresiduesymbol. 
