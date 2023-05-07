Download Link: https://assignmentchef.com/product/solved-ie613-assignment1
<br>
<strong>Question 1 </strong>Consider the problem of prediction with expert advice with d = 10. Assume that the losses assigned to each expert are generated according to independent Bernoulli distributions. The adversary/environment generates loss for experts 1 to 8 according to Ber(0.5) in each round. For the 9th expert, loss is generated according to Ber(0.5−∆) in each round. The losses for the 10th expert are generated according to different Bernoulli random variable in each round– for the first T/2 rounds, they are generated according to Ber(0.5+∆) and the remaining T/2 rounds they are generated according to Bernoulli random variable Ber(0.5 − 2∆). ∆ = 0.1 and T = 10<sup>5</sup>. Generate (pseudo) regret values for different learning rates (η) for Weighted Majority algorithm. The averages should be taken over at least 20 sample paths (more is better). Display 95% confidence intervals for each plot. Vary c in the interval in steps of size 0.2 to get different learning rates. Implement Weighted Majority algorithm with

η             2log( )       .

<strong>Question 2</strong>Consider the problem of multi-armed bandit with K = 10 arms. Assume that the losses are generated as in Question 1. For each of the following algorithms generate (pseudo) regret for different learning rates (η) for each of the following algorithms. The averages should be taken over atleast 50 sample paths (more is better). Display 95% confidence intervals for each plot. Vary c in the interval [0.1 2.1] in steps of size 0.2 to get different learning rates.

<ul>

 <li>Set η = c<sup>p</sup>2log(K)/KT.</li>

 <li>P. Set η = c<sup>p</sup>2log(K)/KT, β = η, γ = Kη.</li>

 <li>EXP-IX. Set η = c<sup>p</sup>2log(K)/KT, γ = η/2.</li>

</ul>

<strong>Question 3  </strong>In Question 2, which one of EXP3, EXP3.P and EXP3-IX performs better and why?

<strong>Question 4 </strong>Show that for any deterministic policy π there exists an environment ν such that R<sub>T</sub>(π,ν) ≥ T(1 − 1/K) for T rounds and K arms.

<strong>Question 5 </strong>Suppose we had defined the regret by

where I<sub>t </sub>is the arm chosen by the policy π and x<sub>tI</sub><sub>t </sub>is the reward observed in the round t. At first sight this definition seems like the right thing because it measures what you actually care about. Unfortunately,

1-1

1-2                                                                                                                                                           Homework 1: February 7

however, it gives the adversary too much power. Show that for any policy π (randomized or not) there exists a ν ∈ [0,1]<sup>K</sup><sup>×T </sup>such that

<strong>Question 6  </strong>Let p ∈P<sub>k </sub>be a probability vector and suppose Xˆ : [k]×R → R is a function such that for all x ∈ R<sup>k</sup>, if A ∼ p,

k

E[X<sup>ˆ</sup>(A,x<sub>A</sub>)] = <sup>X</sup>p<sub>i</sub>X<sup>ˆ</sup>(i,x<sub>i</sub>) = x<sub>1</sub>.

i=1

Show there exists an a ∈ R<sup>k </sup>such that such that  and.

<strong>Question 7  </strong>Suppose we have a two-armed stochastic Bernoulli bandit with µ<sub>1 </sub>= 0.5 and µ<sub>2 </sub>= 0.55. Test your implementation of EXP3 from the Question 2. What happens when T = 10<sup>5 </sup>and the sequence of rewards is x<sub>t</sub><sub>1 </sub>= I{t ≤ T/4} and x<sub>t</sub><sub>2 </sub>= I{t &gt; T/4}?

<strong>Submission Format and Evaluation: </strong>Your should submit a report along with your code. Please zip all your files and upload via Moodle. The zipped folder should named as YourRegistrationNo.zip e.g.‘154290002.zip’. The report should contain two figures: first figure should have one plot corresponding to algorithm in Q.1 and the other should have 3 plots one corresponding to each algorithm in Q.2. For each figure, write a brief summary of your observations. We may also call you to a face-to-face session to explain your code.

<strong>Note: </strong>Please calculate (pseudo) regret for each algorithm in Q.2 for a given set of parameters as follows:

Let µ<sup>i</sup><sub>t </sub>denote the mean of arm i in round t. Suppose an adversary generates sequence of loss vectors and an algorithm generates sequence of pulls, the (pseudo) regret for this sample path is

)]                                                                        (1.1)

T                                      T

= XµItt − minXµit                                                                                                                     (1.2)

i

t=1                                  t=1

Note that in this calculation we only considered the mean values of losses, not the actual losses suffered. It is Okay if this value turns out to be negative. There is no expectation over random choices of I<sub>t</sub>s here. Now generate 20 such sample paths and take their average.