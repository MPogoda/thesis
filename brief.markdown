Convolution
===========

1. Is some form of integral transformation.
2. Unit impulse (δ) is some kind of zero element.

Deconvolution
=============

f * g + ε = h

If we don't know g in advance, we need to estimate it. Usually, it's done
using methods of _statistical_ _estimation_.

Point spread function
=====================

Simple definition: image of point what we've get with same instrument.
The more sharper edge of that image is (no blur near edges) → the more
optically perfect is instrument.

Harder definition: a mathematical function that describes the distortion in
terms of the pathway a theoretical point source of light takes through the
instrument.

Digital image processing
========================

1. Assume that instrument is optically perfect, LOL.
2. Assume that image is convolved with point spread function.

If PSF is unknown, it may be possible to deduce it systematically trying
different possible PSFs and assessing whether the result has improved.
It's called *BLIND* deconvolution.

The most common _iterative_ algorithm is Richardson-Lucy deconvolution.
Wiener deconvolution is the most common non-iterative algorithm.

Richardson-Lucy deconvolution
=============================

We can use this algorithm on small chunks of image more effectively, than
Wiener.

Wiener deconvolution
====================

y(t) = h(t) * x(t) + n(t)

x(t) is some input signal at time t
h(t) is known impulse response (PSF)
n(t) is noise signal
y(t) is observed signal.

Goal is to find g(t) so that we can estimate x(t):
  X(t) = g(t) * y(t)

X(t) is an estimate of x(t) that minimises the mean square error.

Wiener deconvolution uses Fourier transforms.

In case of image processing t and f in Fourier transforms became
two-dimensional.

Fourier transform
=================

Represents frequency domain of signal.
TODO:

