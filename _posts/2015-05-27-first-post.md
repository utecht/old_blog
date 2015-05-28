---
layout: post
title: Formatting Test Post
tags: test
---

This is a post to test various formatting.

Here is some python
{% highlight python %}
from rdflib import Graph

g = Graph()

g.parse("m5.nt", format="nt")

print(len(g))
print("Writing n3...")
with open("movies.n3", "w") as f:
	f.write(g.serialize(format="n3"))
print("Wrote n3")

print("writing turtle")
with open("movies.turtle", "w") as f:
	f.write(g.serialize(format="turtle"))
print("wrote turtle")

print("writing xml")
with open("movies.xml", "w") as f:
	f.write(g.serialize(format="xml"))
print("wrote xml")
{% endhighlight %}

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3

> this is a block quote
> this is still part of the block quote?

> this is another line in the block quote