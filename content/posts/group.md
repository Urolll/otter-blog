+++
date = '2024-12-31T20:47:18+07:00'
draft = false
title = 'An Introduction to Group Theory (Part 1)'
math = true
+++

In this first part, we will simply define what a group is. Before we can understand what a group is, we need to look at some other concepts. 
We will build our intuition from each of the concepts we learn one by one.

## What is a Set?

A **set** is a collection of unique thing. We will call each thing in a set an **element** of that set from now on. 
We can have as many elements in a set as we want.

For example:

O is a set of otters with 3 distinct otters named o1, o2, and o3. Each otter is an element of O.

We can denote it like this: O = {o1, o2, o3}. 

This set O is **finite**. We can count how many otters we have, it's 3!

\\( \mathbb{N} \\) is a set of all counting numbers starting from 1.

We can denote it like this: \\( \mathbb{N} \\) = {1, 2, 3, 4, 5, ...}

This set \\( \mathbb{N} \\) is **infinite**. We can count how many numbers we have, but it will take forever to reach the last number! 
Will we even reach the last number? 

We can use membership to denote if an element is in a set.

\\( o1 \in O \\) means o1 is an element of O.

\\( o4 \not\in O \\) means o4 is NOT an element of O.

This is all we need to know about sets. Hopefully, we are still on the same page.

## What is an Operation?

An **operation** is simply a rule performed on an element or elements in a set. It tells us how many elements we take into the operation and return another element that may or may not be in the set.

Let's take the set \\( \mathbb{N} \\) again. 
We can denote an operation called negate, with symbol "-" that takes in one element of \\( \mathbb{N} \\) and returns the negative of that element.

For example,

\\( 5 \in \mathbb{N} \\) and -(5) = -5

Note that the element \\( -5 \not\in \mathbb{N} \\) so this operation does not ensure our result with be in the set \\( \mathbb{N} \\) we defined it on.

A **binary operation** is a specific type of operation that takes in exactly 2 elements in a set S and return another element that may or may not be in S.

An example of a binary operation is subtraction, which we could also denote with symbol "-".

For example,

\\( 3 \in \mathbb{N}, 2 \in \mathbb{N} \\) and 3 - 2 = \\( 1 \in \mathbb{N} \\)

Question: Does this mean that the operation "-" will always return a result that is in \\( \mathbb{N} \\)?

Answer: No, of course not!

\\( 3 \in \mathbb{N}, 2 \in \mathbb{N} \\) and 2 - 3 = \\( -1 \not\in \mathbb{N} \\)

## What is a Magma?

**Closure** is a property of an operation. 
In fact, when we talked about operations, we have already alluded on what closure could mean. 
An operation defined on set S is closed if the result of the operation always gives an element that is in S.

Question: Is "-" defined on 1 input and 2 inputs closed?

Answer: Neither of them are closed, we already discussed why!

A **magma** is a set S with a closed binary operation.

Let's consider the set T = {TRUE, FALSE} and an operation XOR. 
XOR is defined so that the result is TRUE if only 1 of the inputs is TRUE, and FALSE otherwise.

In other words,

FALSE XOR FALSE = FALSE

FALSE XOR TRUE = TRUE

TRUE XOR FALSE = TRUE

TRUE XOR TRUE = FALSE

Question: Is set T with the operation XOR a magma?

Answer: Yes, because we tried every possible combinations of input, and all of them result in either TRUE or FALSE, which are elements of set T!

## What is a Semigroup?

An operation "\\( \circ \\)" is said to be **associative** in set S if it satisfies the following condition:

$$
a \circ (b \circ c) = (a \circ b) \circ c  = a \circ b \circ c = \qquad a, b, c \in S
$$

This seems like an inoffensive statement, but having this constraint holds a lot of weight.
Essentially we are able to group the parenthesis around our binary operation in many ways, and removing the parenthesis should not affect the outcome at all.

We can of course try to extend this to more than 3 elements. For example, with 4 elements in S:

$$
a \circ b \circ c \circ d
$$

We can group the parenthesis in the following ways:

(1) \\( ((a \circ b) \circ c) \circ d \\)

(2) \\( (a \circ (b \circ c)) \circ d \\)

(3) \\( a \circ ((b \circ c) \circ d) \\)

(4) \\( a \circ (b \circ (c \circ d)) \\)

(5) \\( (a \circ b) \circ (c \circ d) \\)

Question: Knowing that our operation is associative, can we prove that all of the above are equivalent?

Answer: Yes! Here is the proof!

Focusing on (1) and (2), if we ignore the d for a moment, the first 3 terms look just like our definition of associativity.
Since \\( a \circ (b \circ c) = (a \circ b) \circ c \\), we know that operating both on d will give the same outcome, so (1) = (2).

Focusing on (2) and (3), if we consider \\( b \circ c \\) as a single element, then we can also apply associativity on a, \\( b \circ c \\), d.
So, (2) = (3).

Focusing on (3) and (4), we can use the same logic as when we proved (1) = (2), but let a take the role that d took previously. This means (3) = (4).

Focusing on (4) and (5), we can treat \\( c \circ d \\) as a single element and use the same logic as when we proved (3) = (4). This means (4) = (5).

So, all of the five statements are equivalent. We just extended associativity to 4 elements, and we can keep doing this to as many elements as we want. This is a direct consequence of associativity.

Question: Is XOR defined previously associative in set T.

Answer: Yes! You can try it yourself case-by-case on 3 inputs! We brute force every possible outcomes!

A **semigroup** is a set S with a closed and associaitive binary operation. 

Question: Is every magma a semigroup?

Answer: Yes!

Question: Is every semigroup a magma?

Answer: No! Only associative magmas are semigroups!

Let's go through another example. We define a set of otters O with 2 elements, o1 and o2.
We also define an operator "+" in the following way:

o1 + o1 = o2

o1 + o2 = o2

o2 + o1 = o2

o2 + o2 = o1

If we apply an element with itself, we invert it by returning the other element. 
Otherwise, we get the element o2.

Question: Is the set O = {o1, o2} with the operation "+" a semigroup?

Answer: No! We can give a counterexample!

(o1 + o1) + o2 = o2 + o2 = o1

o1 + (o1 + o2) = o1 + o2 = o2

So, \\( (o1 + o1) + o2 \ne o1 + (o1 + o2) \\), which means "+" in set O is not associative, so it does not form a semigroup.

## What is a monoid?



## What is a group?

