---
layout: post
title:  "The Stable Sort"
date:   2015-08-29 14:10:21
categories: stable sorting algorithm
---
When it comes to sorting a list, stability of the algorithm is something that is often talked about in documentation, but not always understood by those just getting into programming. While working through implementing a simple stable insertion sort today, a few colleagues of mine were curious about why algorithms would be stable.

To answer the first obvious question: "What is a 'stable' sort?" A stable sort is one that maintains the order of the items in the list that have the same sorted value. For instance, say we had a list of 4 people: "Sally Sue, Jason Bourne, Jason Steel, and Manny Justice." In this sort, we have chosen to sort based upon the first letter of each person's first name. It's easy to determine that the last two items of this list would be Manny Justice and Sally Sue, but what about the first two? Depending on how you create your algorithm, as well as your intention of what the algorithm should do, what happens can vary.

However, since this is a stable sort we're talking about, the answer is actually relatively simple. Since Jason Bourne is earlier in the list than Jason Steel, Bourne should be first in the list. But why does this matter? Remember that numbers and simple names aren't the only things that can be sorted, and often times we can only sort based upon a single facet of a whole object (imagine sorting 20 objects, some of which have similar values - by which we sort - but entirely different properties. It can be important that the specific order of these objects remains in place relative to that single value that we sorted by). It's for this reason that a stable sort can be important. So consider which sorting algorithms you use wisely!

But what if you don't care about the order of individual objects? What if you just need an array of numbers sorted for some data? Then feel free to use unstable sorts! In many cases, unstable sorts will be quicker than their stable counterparts, although they won't keep track of order. So use the sorts that will perform best for you, while still keeping in mind your needs for your programs!