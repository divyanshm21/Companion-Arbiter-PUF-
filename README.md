# Readme
Below is a implementation of companion arbiter PUF arbiter PUF is a chain of k multiplexers,
each of which either swaps the lines or keeps them intact, depending on what is the challenge
bit fed into that multiplexer. The multiplexers each have delays which are hard to replicate but
consistent. Let tu, tl respectively denote the time for the upper and lower signals to reach the
finish line and let Δ def = tu −tl denote the difference in the timings. Note that Δ can be negative
or positive. Assume that tu = tl never happens i.e., Δ is never exactly zero. If the upper signal
reaches the finish line first i.e. Δ < 0, the response is 0 else if the lower signal reaches first i.e.
Δ > 0, the response is 1.
![image](https://github.com/user-attachments/assets/f05bdea7-195e-4ca0-a53a-fde105fb4ab1)
We will create a PUF using multiple arbiter PUFs and decided
to call it a Companion ArbiteR PUF (CAR-PUF for short). A CAR-PUF uses 2 arbiter
PUFs – a working PUF and a reference PUF, as well as a secret threshold value τ > 0. Given
a challenge, it is fed into both the working PUF and reference PUF and the timings for the
upper and lower signals for both PUFs are measured. Let Δw,Δr be the difference in timings
experienced for the two PUFs on the same challenge. The response to this challenge is 0 if
|Δw − Δr| ≤ τ and the response is 1 if |Δw − Δr| > τ where τ > 0 is the secret threshold value
**We show that there exist a linear model that can perfectly predict
the responses of a CAR-PUF and this linear model can be estimated fairly accurately if given
enough challenge-response pairs (CRPs).**
