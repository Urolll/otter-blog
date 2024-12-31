+++
date = '2024-12-31T20:47:18+07:00'
draft = false
title = 'What is a Group?'
math = true
+++

Before we can understand what a group is, we need to look at some other concepts.

## What is a Set?

A **set** is a collection of unique things, which we would call **elements** from now on. You can have as many elements in a set as you want.

For example:

O is a set of otters with 3 distinct otters named o1, o2, and o3.

We can denote it like this: O = {o1, o2, o3}. 

This set O is **finite**. We can count how many otters we have, it's 3!

N is a set of all counting numbers starting from 1.

We can denote it like this: N = {1, 2, 3, 4, 5, ...}

This set N is **infinite**. We can count how many numbers we have, but it will take forever!

We can use membership to denote if an element is in a set.

\\( o1 \in O \\) means o1 is an element of O.

\\( o4 \not\in O \\) means o4 is NOT an element of O.

This is all we need to know about sets. Hopefully, we are still on the same page.

## What is an Operation?

An **operation** is simply a rule performed on an element or elements in a set. It tells us how many elements we take into the operation and return another element that may or may not be in the set.

Let's take the set N again. We can denote an operation called negate, with symbol "-" that takes in 1 element of N and returns the negative of that element.

For example,

\\( 5 \in N \\) and -(5) = -5

Note that the element \\( -5 \not\in N \\) so this operation does not ensure our result with be in the set N we defined it on.

A **binary operation** is a specific type of operation that takes in exactly 2 elements in a set S and return another element that may or may not be in S.

An example of a binary operation is subtraction, which we could also denote with symbol "-".

For example,

\\( 3 \in N, 2 \in N \\) and 3 - 2 = \\( 1 \in N \\)

Question: Does this mean that the operation "-" will always return a result that is in N?

Answer: No, of course not!

\\( 3 \in N, 2 \in N \\) and 2 - 3 = \\( -1 \not\in N \\)

## What is a Magma?

**Closure** is a property of an operation. An operation defined on set S is closed if the result of the operation always gives an element that is in S.

A **magma** is a set S with a closed binary operation.

Let's consider the set M = {TRUE, FALSE} and an operation XOR. XOR is defined so that the result is TRUE if only 1 of the inputs is TRUE and FALSE otherwise.

In other words,

FALSE XOR FALSE = FALSE

FALSE XOR TRUE = TRUE

TRUE XOR FALSE = TRUE

TRUE XOR TRUE = FALSE

Question: Is set M with the operation XOR a magma?

Answer: Yes, because we tried every possible combinations of input, and all of them result in either TRUE or FALSE, which are elements of set M!

## What is a semigroup?


## What is a monoid?


## What is a group?
