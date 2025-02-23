# CS7150-Homework-4

This homework consists of six short notebooks, tracing the history of latent-variable
generative modeling strategies. These all go beyond the autoregressive approach that is so
successful in language modeling that we learned in the first half of the course.

Whereas the autoregressive approach factors the target distribution into a sequence
of tokens (each one modeled as a conditional probabilty distribution that
depends on the previous tokens) the latent-variable approach models the distribution
as a process or a function f that transforms a boring distribution z (e.g., a random
vector drawn from a normal distribution) into an interesting distribution x = f(z)
that imitates the target distribution.

In the first five notebooks you will use a simple "swiss roll" distribution as the
target. In all these the goal will be to learn some process f, so that x = f(z)
looks like a "swiss roll" when z is drawn from a normal distribution.

You will see that in some of the methods, the f to learn is directly a neural network,
whereas in other cases, f is a process that incorproates a neural network that
plays a particular role within that process.  A couple of the methods also train a
supplementary neural network to help.  All of these different schemes are designed
to put the neural network in a situation that makes it possible to optimize it easily
towards the goal of making f(z) imitate the target distribution, if all we have as
training input is a big set of samples.

In the final notebook, you will apply diffusion modeling to make an MNIST image
generative model.  (If it interests you, for extra credit, at the end of that
last notebook you can implement any of the other methods (VAE, GAN, etc) to
implement and visualize an MNIST generator.)
