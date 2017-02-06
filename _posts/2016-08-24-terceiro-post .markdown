---
layout: post
title:  "Notes about article"
---

article

key concepts

There are 2 types of automic summarization, abstractive and extractive.

Abstractive - create new sentences, more difficult
Extractive -  use representative sentences from the input 

we can divide extractive summarization in 2 components:
 - Summarization framework
 - similarity measures used to compare sentences

 <h1>Framework</h1>

 Extractive summarization is seen as a optimization problem where we are going to use "monotone nondecreasing submodular set functions", this means:

 Set function -  input is a set and output a number

 this submodular function is like a convex function so we can minimize, in summarization we can interpret as the combination of 2 terms, one which encourage the summary to be representative of the corpus and the other that positively rewards diversity

A function is submodular if it complies the following property: when you add a set to a solution "A" the improvement is worst than adding the same set to a subset of "A".
Submodularity is a discrete version of concavity. 
see more:
https://www.quora.com/What-is-submodular-optimization


Diminishing returns - explains the adding of more workers for example to a company, so if a quantity of a thing is increased and the others remain constant, the total production is going to fall

example: A common sort of example is adding more people to a job, or assembling a car on a factory floor. At some point, adding more workers causes problems such as workers getting in each other's way or frequently finding themselves waiting for access to a part. In all of these processes, producing one more unit of output per unit of time will eventually cost increasingly more, due to inputs being used less and less effectively.
source: wikipedia


In the context of automic summarization, adding a sentence to a small set of sentences(summary) makes greater improvement(contribution) than adding to a large set . the aim is to find a summary that maximizes diversity on sentences and the coverage of the input text.

F(S)= L(S) + lambda*R(S)

S-summary
L(S) - coverage of input text
R(S) -  diversity reward function
lambda -  tradeoof coefficient 

lambda allow us to define the importance of coverage vs diversity

see article, there is a function with summation

<h1> similarity measure</h1>

measuring similarity between setences TD-idf

So, each vetor has values that represents weights(td-idf) of words in a sentence, a setence has a vetor associated
tf - # of occurences of word w in sentence i and j
idf - inverse document frequency

<h1> deep learning </h1>

mentions about auto-encoder, feed forward, recursive tree

<h1> word embeddings </h1>

a word embedding is a continuous vetor representation that capture semantic and syntactic info about a word


CW VETORS

check later

CONTINUOUS SKIP NGRAM

model trained to predict the context of a word

<h1> phrase embeddings</h1>

sentences need to be compared

simple case, consider a vetor setence a sum of vetores which represent a word, without regarding word orders

recursive auto encoder, taking into account word order

cosine similarity as a measure 



