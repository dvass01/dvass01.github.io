---
layout: post
title:  "Helpful Features in Python"
date:   2015-04-19 20:10:00
categories: python language features
---
I learned some very helpful features about Python today after reading Sahand Saba's blog entitled Math u Code.  One of the most helpful for me involved double-ended queues.

The collections module enables Python users to utilize the deque container, which supports some useful methods such as appendleft, extendleft, popleft, reverse, rotate and others.  I have included an example below to illustrate how these methods are used.  I plan on using these deque objects in my own work.  As I write this post, I am thinking of situations in the past where they would have come in very handy.


import collections
from collections import deque
c = collections.deque()
c.append(7)
c.extend([5,3])
c
deque([7, 5, 3])
c.extendleft([0])
c
deque([0, 7, 5, 3])
c.rotate(3)
c
deque([7, 5, 3, 0])
c.appendleft(9)
c
deque([9, 7, 5, 3, 0])
c.popleft()
9
c
deque([7, 5, 3, 0])
c.extendleft([6,8])
c
deque([8, 6, 7, 5, 3, 0])
c.append(9)
c
deque([8, 6, 7, 5, 3, 0, 9])
c.reverse()
c
deque([9, 0, 3, 5, 7, 6, 8])
