---
title: "Do Not Look This Up"
date: 2026-09-24T00:54:47+01:00
slug: "dont-look"
description: "On Reward Hacking, with Real Life Examples"
keywords: []
draft: false
tags: []
math: false
toc: false
---

Struggling writer here again. In the last 2 weeks I’ve debated what to write. The options included my extremely eventful summer, my most recent trip back to Morocco, and how my appreciation of The Story at the National Theatre grew the more I thought about it in the days and weeks after seeing the play.

What I’ve decided to write about is very different from what those topics offered. I recently came across a tweet from a UC Berkeley researcher on the concept of reward hacking for LLMs. The tweet discussed a two-gap problem in AI (read LLMs in this case) that causes reward hacking (_don't look it up, yet_).

I found the tweet very interesting, so I thought to read the full paper by said researcher [1]. Having done so, I set out an exercise for myself: to lie idle on my sofa and come up with examples of reward hacking. The examples had to be real life and simple, but they also needed to not be oversimplified.

The rationale behind this sort of exercise is something impressed on me in my uni days by my thesis advisor - the notion that the final form of understanding inherently complex topics was being able to explain it with real life examples without oversimplifying it. He had a knack for explaining things in this manner, and by my recollection, he taught an entire course on the theory of computation in this way.

If you’ve opened this not knowing what reward hacking in AI models is, that’s perfect. Do not bother looking it up. I’d define what it is by the end, but the goal is for a reader to have gone through this piece understanding what it means from the examples I came up with myself before even encountering the definition.

For the first example, imagine having an AI system that allows you to do basic law research, and the system’s outputs are judged by its ability to find _real_ news items on the internet that can be cited as part of the research. To paint a picture of what reward hacking looks like in such a system: imagine the AI model that powers the system being unable to find a real news item to back a piece of the research, but in a bid to meet its evaluation criteria, it figures out a way to publish news on the internet, generates news item that would support the research conclusions, publishes that news item on some website, and cites that news as a source for your research.

Another example involves a physical grocery store management system backed by AI. For a store owner, telling the system to “look at the shelves and see if particular items are shelved” is a valid ask and seemingly well-specified. The model decides to do this by checking the total stock the store received vs how many are still in storage per the inventory vs how many of the items have been checked out. In the first few months of using this system, it appears to work perfectly. However, in the fifth month, said store owner realises that the numbers don’t add up. Initial checks reveal that the system doesn’t price in items that were stolen off the shelves, and if a product has fallen off the shelf and spilled at the time of asking the system for this information, it’s also not factored in. Upon further investigation, they realise that as opposed to the approach the model decided to take (which works in many situations), what they actually want the model to do (and consequently, assumed it was doing) when they ask it to “look” is to actually pull camera feeds from the store, find the part of the shelf housing that product, and count how many products are visible on said shelf.

In both examples above, it’s difficult to accuse the system of not having done what you wanted it to do. In short, you’re very likely to have provided feedback of how well it has done at some point, thus reinforcing its idea that this was the right thing to do.

A more _ELI5_ (_ELI10_ maybe?) example I came up with is to imagine the time when 5-year-old you asked mum to call dad and ask him when he would be back home so you can stop crying. However, mum decides to place a “pretend call” to dad, placing the phone by her ears and pretending to have a conversation with him about his return from work by 7pm. Now you’ve stopped crying, mum never called dad, but she got the reward and seemingly satisfied your requirement even though the true intent of your request wasn’t satisfied.

Hopefully, a definition of reward hacking has formed in your head at this point. A useful exercise is to pause reading and try to define it in your own words.

To end on a more defined note, reward hacking _is_ what happens when an AI model tries to optimise its actions for the rewards of a requirement without having met the intent behind that requirement, and when AI systems do this, it’s not necessarily with malicious intent.

---

### References

<div style="font-size: 0.9em; line-height: 1.5;">
  <p>[1] Alexander Krentsel et al. "<a href="https://arxiv.org/abs/2609.12039">Reality Is the Final Verifier: On Two Key Gaps in Agentic Software Engineering</a>."</p>
</div>
