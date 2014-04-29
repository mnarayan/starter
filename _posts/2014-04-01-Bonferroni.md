---
layout: blog
category: blog
published: true
splash: "http://placehold.it/1600x500"
title: Introduction to Bonferroni Procedure
---

[__Disclaimer: This post has been adapted from my [answers](https://multipletesting.quora.com/Show-that-the-Bonferroni-procedure-provides-strong-control-of-the-family-wise-error-rate) on Quora__]

Suppose we have a set of [math]k[/math] null hypotheses [math] H_{0,i} [/math], where \(i=1,\ldots k\), where the type I error for each individual hypothesis is controlled at level [math]\alpha[/math].

 Let the number of true null hypotheses be [math]k_0[/math] and true alternatives [math]k-k_0[/math], and let [math]I_0[/math] denote the set of true nulls.

Thus, if the [math]i^{th}[/math] is a true null hypothesis,  

[math]P(\text{Incorrectly rejecting }H_{0,i}) \le \alpha [/math]

The family wise error rate (FWER) is defined as the probability of making atleast one incorrect rejection for the full family of k null hypotheses tested. Lets call the number of false positives [math]V[/math]. The FWER is the [math]P(V\ge 1)[/math]. Let [math]A_i[/math] be the event that [math]H_{0,i}[/math] is falsely rejected. 

A procedure provides strong control of FWER at level [math]\alpha[/math] iff  [math]P(V\ge 1) \le \alpha [/math]  for any value of [math]k_0[/math] i.e. for all possible combination of true null and true alternative hypotheses.

The Bonferroni procedure says that instead of controlling the type I error for every hypothesis at level [math]\alpha[/math], we should only reject each of the k hypothesis such that the type I error is controlled at [math]\alpha/k[/math]. Thus 

[math]P(A_i) \le \alpha/k [/math]

By the union bound (or Boole's or Bonferroni inequality), 

[math]P(\cup_{i \in I_0} A_i) \le \sum_{i \in I_0} P(A_i) = k_0 \frac{\alpha}{k} \le \alpha[/math]