---
title: "Optimizing_a_Python_function"
date: 2024-04-12T12:33:38-05:00
draft: true
toc: false
images:
tags:
  - untagged
---

One of my principal roles working as contributor on the CryptographicEstimators library, is to drop the usage of Sage, a huge library to work with maths, and that provides a lot of highly optimized numeric-theoretic functions (integrating multiple low-level libraries written in C). Our reason to do that is because it will make the library more lightweight and easy to install and understand; therefore we want to drop sage as a dependency in the near future.

Recently I was tasked to write a pure Python function that replaces the use of `sage.arith.misc.is_prime_power`, a function that given an integer, tell if it is a power of some prime or not. To my surprise, this was a very interesting task because ended up requiring me to build a benchmarking python module, learn about new data structures and internals in Python, and even make some code profiling to check bottlenecks. Because it was a great experience, I want to share with all of you what the process was, so maybe if you ever need to make something similar, at least have in mind some useful steps to tackle the task!

# Understanding the task, and giving a first solution

As I say above, I was assigned to write

## Writing steps

- Understanding the task, how it will be approached, and giving a first solution

Qué función debo atacar, cómo lo quise hacer, cuál solución propuse, y cuáles fueron comparativamente los resultados de esa primera solución.

-

https://docs.python.org/3/howto/functional.html
