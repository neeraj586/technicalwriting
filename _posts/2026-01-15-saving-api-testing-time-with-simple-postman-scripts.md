---
title: Saving API Testing Time with Simple Postman Scripts
description: Tips on how to save time during API testing using simple scripts in Postman.
date: 2026-01-15 19:42:00 +0530
categories: [productivity hacks]
tags: [postman, api-testing, productivity]
author: neeraj
---

Recently, I was thinking about ways to save time while testing APIs.

Before documenting anything, I always test the APIs myself and validate the changes. That’s the ideal approach if you ask me; you know exactly what you’re writing about. But over time, I realised this step eats up a lot of my capacity.

I considered automating API testing end to end. But writing detailed use cases and maintaining scripts for every scenario would take more time than manual testing itself.

But I realised that while full automation may not be worth it, work like manually verifying certain expected parameters in a response can be automated, using simple scripts in Postman.

If you’re a tech writer who follows a similar workflow, this might help. It’s not complicated or path-breaking. Just something I figured out recently and wanted to share.

## Use case

New parameters are added to an API response to capture time in ISO format.  
You need to ensure that for every date field, a corresponding ISO field exists.

## Traditional approach

1. Run the API.  
2. Manually scan the response.  
3. Check whether the new ISO parameters exist.  
4. If something is missing, flag it to the developer.  
5. If everything looks good, update the documentation.

This works—but it’s easy to miss things.

## Requirement

You want verification of the new parameters to happen automatically, so nothing slips through because of manual oversight.

## Solution

Write a Postman test script that validates the presence of ISO shadow fields for all date fields in the response.

## How to do it

Use GPT (or any LLM) to generate the script. For this use case, I used the following prompt:

```text
Write a Postman test script that validates date fields in an API response.

Requirements:
- Detect all fields whose values represent dates or date-times.
- For each date field, check that a corresponding ISO shadow field exists.
- A shadow field is identified by the same base name with ISO or TimeISO appended.
- Create a separate Postman test for each field, not a single aggregated assertion.
- The script must work recursively for nested objects and arrays.
- Ignore fields that are already ISO fields.
- Test results should clearly indicate which specific field is missing its ISO shadow field.

Output:
- Provide only the Postman test script.
- Do not include explanations unless necessary.
````

## Run the check

1. Copy the prompt output.
2. Paste it into the Scripts section in Postman.
3. Run the API.
4. Review the results in the Test Results panel.

![Postman Script Example](/assets/img/posts/postman-scripts/postmanscript.png)

You’ll now get clear, field-level failures for any missing ISO parameters—without manually scanning the response every time.




