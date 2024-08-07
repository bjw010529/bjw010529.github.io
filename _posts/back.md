---
layout: bilevel
title: Notes on bilevel optimization
description: "based on \"A review on bilevel optimization: From classical to evolutionary approaches and applications\" as well as other materials "
tags: bilevel optimization
giscus_comments: true
date: 2024-07-24
featured: true
toc:
  sidebar: left
authors:
  - name: Jiawen Bi

# bibliography: 2024-07-24-bilevel.bib
bibliography: 2018-12-22-distill.bib

# Optionally, you can add a table of contents to your post.
# NOTES:
#   - make sure that TOC names match the actual section names
#     for hyperlinks within the post to work correctly.
#   - we may want to automate TOC generation in the future using
#     jekyll-toc plugin (https://github.com/toshimaru/jekyll-toc).
toc:
  - name: Bilevel Optimization
  - name: Classical Approaches
    subsections:
      - name: Single-level Reduction
      - name: Penalty Function Methods
      - name: Trust-region Methods
  - name: Moreau Envelope for bilevel optimization

# Below is an example of injecting additional post-specific styles.
# If you use this post as a template, delete this _styles block.
_styles: >
  .fake-img {
    background: #bbb;
    border: 1px solid rgba(0, 0, 0, 0.1);
    box-shadow: 0 0px 4px rgba(0, 0, 0, 0.1);
    margin-bottom: 12px;
  }
  .fake-img p {
    font-family: monospace;
    color: white;
    text-align: left;
    margin: 12px 0;
    text-align: center;
    font-size: 16px;
  }

---

## Bilevel Optimization

First, about bilevel optimization. These problems contain two levels
of optimization tasks where one optimization task is nested
within the other. They are called **Upper Level** problem and **Lower Level** problem, respectively.<d-footnote>Footnote for test.</d-footnote>

The bilevel optimization problem can be expressed as a constrained optimization problem as follows:

$$
\min_{x \in X, y \in Y} F(x, y) \qquad \text{s.t.} \qquad y \in S(x)
$$

where $$ S(x) $$ denotes the set of optimal solutions for the constrained Lower Level problem 

$$
\min_{y \in Y} f(x, y) \qquad \text{s.t.} \qquad g(x, y)\le 0
$$

***

## Classical Approaches

### Single-level Reduction

### Penalty Function Methods

Penalty function methods deal with the bilevel optimization problems by adding penalty terms that measure the extent of violation of the constraints.
The idea is trivial in optimization, but the bilevel hierarchy was still maintained and the reduced problem was still difficult to solve.

In <d-cite key="ishizuka1992double"></d-cite>, the problem is reduced into a single level problem by replacing penalty term with its KKT conditions.
Also, there are many ways to set penalty. 
For instance, in <d-cite key="yao2024constrained, lu2024first"></d-cite> they consider using penalty term to convert bilevel 
optimization problems to minimax problems.<d-cite key="gregor2015draw"></d-cite>

### Trust-region Methods

Not interested right now


***

## Moreau Envelope for bilevel optimization

For test.


