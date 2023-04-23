# Interpolation Analytics

This article focuses on interpolation subject, in particular, the interpolation of curve bootstrapping. Both linear spline and cubic spline are studied. Although there are a number of advantages to using piecewise cubic splines, there is one major drawback which leads us to go in favour of linear splines.  This drawback stems from the fact that the perturbation of one point will affect another point.

We will show a graphical illustration later of how the perturbation of one point will affect other points.  As a result, we recommend that linear splines be used to construct the various curves rather than higher order polynomial splines.

Given a set of discrete data points  , one can use linear interpolation between successive points to build a piecewise linear interpolant of the data points  :

One can then use this to approximate other points on the curve.  The advantage of linear interpolation is its simplicity and, in many cases, it provides an adequate approximation.  A disadvantage is that the approximating curve is not smooth (since the derivative is in general discontinuous at given data points) even though the real curve may in fact be smooth. 

Another method of interpolation is to fit a series of linked cubic polynomials.  Consider an interpolant that allows curvature between the data points and requires the first and second derivatives to be continuous throughout the interval.  Furthermore, assume that the interpolant linking the data points is a cubic polynomial of the form subject to the following constraints:

The first constraint is the interpolation of  ; the second constraint is the continuity of the interpolant and the third and fourth constraints are the continuity of the first and second derivatives respectively.  A final condition is to set the change in slope at the ends of the curve equal to zero (for a natural cubic spline).  

Hence, with cubic splines, the curve has to go through each data point but neither the curve nor its slope can be kinked at any point.  The gap between each data point is represented by a unique polynomial that relates to the next “piece” in a chain by having its slope and rate of change of the slope be equal to that of its neighbour at the point at which they join.  

A simple example below shows how three data points are linked (at x1, x2, x3) with two cubic splines.  

Each section of the curve is a cubic polynomial. First and second derivatives are equal where curves join:

Reference:

https://finpricing.com/knowledge.html

