# yt-zipf
HW - Statistical Methods in Data Science

### Exercise 01: People have the power (. . . law. . . )
##### Introduction
In this exercise we focus on the so called power law family of distributions. An interesting aspect of these distributions is
that, unlike many others we have seen, their variance can be extremely large or even infinite. As a result, certain methods we
usually rely on in probabilistic arguments, such as concentration of the sum of random variables (i.e. Chebyshev or Hoeffding
inequalities), may not apply.
Power laws and related distributions may initially appear surprising or unusual, but in fact they are quite natural, and arise
easily in many applied setups. For example, suppose we want to study the number of times a word appears in all the books
printed in English over a year, for example, all across Europe. Some common words, such as “the”, “of”, and “an”, appear
remarkably frequently, while most words would only appear at most a handful of times describing an extremely right skewed,
very long tailed distribution.
This is just an example. In practice, many other phenomena share this property that the corresponding distribution is
not well concentrated around its mean, such as the sizes of cities, the strength of earthquakes, the distribution of wealth
among families, and the degree distribution of real networks (see below). For many such examples, a power law has been
shown to provide a very plausible model for their distribution.

##### Your Job
1. Take a look at basic tools to deal with graphs in R such as the igraph and ggnet packages.
2. Write a program in R to simulate the preferential attachment process, starting with 4 pages linked together as a directed
cycle on 4 vertices, adding pages each with one outlink until there are 1 million pages, and using γ = 0.5 as the probability
a link is to a page chosen uniformly at random and 1 − γ = 0.5 as the probability a link is copied from existing links.
Simulate a small number M of nets and draw a plot of their empirical degree distribution, showing the number of vertices
of each degree on a log–log plot. Also draw a plot showing the complimentary cumulative degree distribution – that is,
the number of vertices with degree at least k for every value of k – on a log–log plot.
Does the degree distribution appear to follow a power law or a Poisson? Explain showing some evidence supporting your
reasoning.
Dig a bit more into some of the net you generated using the R tools metioned in (1.)
3. Write a program in R to simulate the preferential attachment process as in the previous problem, but now start with 4
pages with each page pointing to the other 3, and add pages each with 3 outlinks until there are 1 million pages. Again
draw the plots of the degree distribution and the complimentary cumulative degree distribution. How do these plots
differ from those in the previous problem? Does the degree distribution appear to follow a power law or a Poisson?
Explain.
4. As mentioned at the very beginning, power laws seem to appear out of the blue almost everywhere...sooo, tell me
something more about it! Start watching this video (https://www.youtube.com/watch?v=fCn8zs912OE&feature=youtu.be) having a close look at the sources cited in its info section.
