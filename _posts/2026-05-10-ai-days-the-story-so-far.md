---
title: "AI Days - The Story So Far"
description: "A personal diary, sort of, on how AI transformed the way we work and its impact so far."
image:
  path: /assets/img/posts/ai-days/cover.png
date: 2026-05-10 13:08:49 +0530
categories: [ai, technical-writing]
tags: [ai, documentation, tools, career]
author: neeraj
---

This is an honest take on my tryst with AI so far. The article is mostly a personal diary. I also expect this to help writers who want to do something but have yet to start or feel blocked.

## Entry of the ChatGPT
Like everyone else, even though I was mind-blown; I also wondered if it was the beginning of the end. But then, eventually, it was considered a tool that makes your work easier and not a replacement, etc and that cooled down the atmosphere a bit.

Overnight, one fine day, DeepSeek came up with models that were as cheap and effective as others. That’s when I realized that unlike other technological changes we have seen, here changes are happening overnight. Still, as everyone said, I considered it an assistant.

## Enter AI tools
Time passed, and AI experts started popping up. At this stage, small companies started emerging that made use of LLM models and built applications to solve specific use cases.
Creation of guides from videos was the first on the list of AI tools that targeted documentation.
Quick backstory: I was a little frustrated and displayed it because I was not included in the decision-making for short-listing this tool. But was the frustration really for that, or was it fear coming out as frustration?
The tool that we tried was an amazing tool, and it could create quality guides if proper videos with voice-overs are given. But, realised we were spending too much time on the tool and the learning curve was more. Hence, dropped it.

## Bot days
In the next tool-wave, AI-powered chatbots that performed semantic search over the docs and returned results started flourishing. We subscribed to a homegrown startup called Threado. But unfortunately, it got shut down (like thousands of other AI start-ups) after a while, and we moved to [Kapa.ai](https://technicalwritingwork.substack.com/p/Kapa.ai). So far, so good.
And this was the moment we felt proud of the documentation. The usage of the documentation skyrocketed and ran into 4000 questions on average every quarter (internal usage alone; we haven’t exposed the bot externally). It also helped us identify gaps in the documentation.

## CustomGPT days

Like many, we just used GPT for grammar fixing and rewriting texts, then to create tables, and so on. Even though the tool gave a glimpse of what lies ahead, after the initial usage, the hype cooled down a little, which only lasted until the next release.
Then came Custom GPT, and we created custom GPTs to review docs, write in MSTP, and so on. But it did not take off much. I see some custom GPTs lying unused in my GPT account. Strangely enough, I see one DB query GPT lying, and I cannot recollect what this was for!

## NotebookLM
NotebookLM is still one tool where usage hasn’t dropped. We still use it to dump all information related to a topic, from Confluence tech docs to voice notes and more. Unlike some other features, like custom GPT, the usage of NotebookLM never dropped. It is always the source of truth for information gathering. All discussions are added there, which helps refer to conversations where a particular point was mentioned. The topper on our list is one with 41 sources. I have seen public notebooks with 1000s of sources though!

## Google AI Studio
Google AI Studio gave us the power to develop tools that we, as non-technical people, would never have built in our entire careers. In fact, this also helped us improve documentation processes. For example, most of our APIs do not have Swagger, and we struggled to document APIs using YAML files, which were often incorrect. People who use ReadMe might relate to this. A cURL-to-OpenAPI spec converter was one of the first tools we created, and we still use it. Other tools include a doc review tool, MSTP checking tool, API doc restructuring, and so on. We had fun building these.

## Cursor
I see Cursor as something that democratized access to the coding ecosystem. We always depended on developers even for confirmation of the data type of a particular field. Cursor empowered us to interact with code, ask questions about it, and actually understand it. A watershed moment for writers.

## Entry of AI-based documentation tools
We use [readme.io](https://technicalwritingwork.substack.com/p/readme.io) , a tool that is an insult to the US itself. A buggy product. Very slow in terms of AI adoption. Hence, we started exploring some new-age tools. Theneo Doc tool was the first doc-based AI tool that came onto my radar. You add an API cURL, and the tool creates a rough structure of the document automatically. A pretty good tool, but migration was a concern and took more time than expected. Cut to the present, we are still on readme because of migration headaches. And also afraid if new age tools will be abel to take up the heavy load of our docs. Compared to other start-ups, ours is a huge documentation.
Readme has shipped a lot of AI features lately. But still, you know, nothing smooth enough.

## Auto-generation of docs based on PR merge
This is another game-changer in documentation. Promptless is the tool we tried for this. It creates a 70% accurate document automatically based on the PR merge, and we only need to handle the rest. But pricing-wise, they charge a bomb and it’s not worth the money. You expect much better for that price. Now with Claude, it is capable of doing what Pomptless does.
Readme has started supporting the same feature. We have access but there are still some bugs on their side, and we are not able to connect the repos till now.

## Age of building tools
In the meantime, I thought of getting this API creation doc built within the company and hired one intern-developer for the same. But I cannot recollect when (a lot of random ideas keep playing around in my head), we started with a different project. It was a Jira analyzer tool.

### JIRA Analyzer tool
We have a lot of tech tickets that get closed citing knowledge gap. The support team identifies the reason as knowledge Gap and closes those tickets. This can be either because of the:
- knowledge gap with the person who raised the ticket or
- gap in the documentation

We could never pick up these tickets and fix the gap in the documentation because of the bandwidth limitations. But here, we decided to get these analyses done through an AI-powered tool that:
- goes through comments and descriptions
- compares them with documentation
- drafts content if a gap is found
- inserts it in the correct location
- creates a GitHub PR and on approval gets added to the docs.

In reality, this added more load to the team as reviewing these is a new addition to our work, but as a side effect, we are learning a lot and covering a lot of gaps in the docs.

### Release Note Bot
This was pretty quick. It started as a Slack bot where you can request release notes for a ticket number, and it generates them. The style guide is predefined, so the output is consistent. The context is pulled from Google Drive (PRDs, tech docs, etc.) and JIRA tickets. Now, our JIRA analyzer tool is a separate tool that can be accessed through a URL, and we added a release note generator to that. To answer your question, how this is different from a ChatGPT or Claude. It is not very different . We get consistent results as the prompts and style are predefined.

## Season of Claude
Personally, I never used Claude and was always using Gemini or GPT and other IDE tools. But Claude hit different. Maybe capability-wise it is nothing different, but for some reasons, it hit a different wave throughout, and an overall “anyone can do anything kind of impression” started spreading from the top of organisation. As a result, we have now been assigned to contribute towards the product management side and involve others in documentation. What started as experimentation now feels like a canary for broader change in the job-role itself.

## What next?
We have a portal where all our tools are accessible to employees.
We are working on creating a space where tools generate content based on the provided context. It seems management wants product managers to take over writing, so we plan to build a platform for that. Claude skills already exist, but a unified platform with predefined instructions would be better.
Automatic API doc generation on PR merge is now possible. If implemented, we can remove external tools.
Release notes can also be auto-generated on PR merge. That is another work in progress.
This is where things stand for now. Still experimenting, still figuring things out.

***

*Disclaimer: This is not an AI generated article. AI has been used to fix grammar only and for thumbnail image.*
