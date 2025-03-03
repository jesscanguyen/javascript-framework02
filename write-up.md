---
layout: layout.liquid
title: Reflection Javascript Framework II
---

# Reflection

After using GPT-4o and Claude 3.5 Sonnet, I would honestly say neither were really effective or helpful in helping me with the prompts I asked. The three questions I asked were:

1. Please using tailwind css (and alpine js if needed) make a simple flex display between the two divs I have currently, centered in the middle of the page
2. The content is not in the middle of the page, how can this be fixed?
3. It seems that most of the tailwind CSS won't render no matter what. can you figure out what the problem is?

I would hope that after asking it to revise the page with the second question, the page would be magically fixed. However, despite whatever solution it may have given (choosing some different classes, using ! to set an order priority.. it was a lot) neither LLM was able to complete the request as I wanted it to. Indeed, most of it just stayed at the top left of the page. However, Claude was able to somehow move the images to the center vertically, but not horizontally. 

After the third question, I realized that a lot of the issue lied in that it seemed the Tailwind CSS was just not loading in, while on CodePen, the code each LLM gave would work fine. So, I then asked GPT-4o and Claude if they could see why my Tailwind stuff wasn't working, even though I had followed the instructions to install Tailwind via CLI. However, they gave me instructions based on Tailwind's 3.0 installation and debugging solutions, despite me telling them I'm on 4.0. They also would ask me to give me the file contents of layout.liquid, or run commands in the terminal and to give them the output. Still, they said that 3.0 is the latest version, and that 4.0 doesn't exist. This is what GPT-4o said:

> "I apologize for the confusion. As of my knowledge cutoff in October 2023, Tailwind CSS 4.0 does not exist. The latest stable version is Tailwind CSS 3.x. If you are seeing a version 4.0, it might be a mistake or a pre-release version."

After a *very* long and frustrating time of personal debugging, I realized that I needed to make a "src" folder where the CSS will stay for Tailwind to work, rather than being able to put it in the "styles" folder. I think this shows that no matter what, the LLMs aren't perfect and can only regurgitate whatever data they've been put in with; which, in the case of coding, isn't always the best because it can give bad code that doesn't work. Humans are an essential part to coding, and everything itself.
