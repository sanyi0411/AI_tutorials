## Anatony of a prompt
- **Role**: Who answers: expert, audience
- **Clarity**: Be unambiguous. Vague instructions produce technically correct results that still miss the point.
- **Goal**: What you want, in one sentence
- **Examples**: One example works better than three sentences of description
- **Context**: Product, audience, occasion, market
- **Material**: Text, data, glossary, examples
- **Format**: Length, structure, language, output
- **Constraints**: What must not appear
- **Adaptibility**: Build the prompt so you can swap out individual parts (template)

```
You are a product manager for industrial pumps. Write a product description for the 2027 catalogue. Your readers are buyers in plant engineering in the UK market. Base it on the data sheet below. No more than 120 words, three paragraphs, British English. No superlatives, no invented technical figures.
```

```
You are a market analyst. Look at our competitor's website [URL].
Compare their value proposition, how they address their audience and their pricing logic with our site [URL].
Output: a table of five points where we should catch up, each with a one-sentence rationale.
At the end, tell me which claims you couldn't verify.
```

```
Cut the following text to [number] words without dropping any facts.
Keep the technical terms, replace filler words, break up long sentences.
Then tell me in one sentence which piece of information you would sacrifice next if it had to be shorter still.
Text: [paste here]
```

### Priming
Priming is part of the prompt. It establishes detailed context, steering the AI model for enhanced relevance. A primer grounds the model in background, goals and frame od reference.

Prime:
```
You are a former management consultant who has advised major Fortune 500 companies on market entry strategies. You possess deep expertise analysing market landscapes and forecasting TAMs.
```

Prompt:
```
With this background, assess the European electric vehicle market for a US manufacturer seeking overseas expansion, focusing on trends, consumer segmentation, unmet needs and areas for differentiation.
```

## Text versus image
- When generating text: plenty of context helps
- When generating image: too many details make the important ones get lost

## Make the AI write the prompt
1. **Note your goal**: Result, audience, format, limits
2. **AI writes the prompt**
3. **Check it**: facts, tone, format
4. **Follow ups**

```
I want to use an AI tool to [goal in everyday language].
Write me a prompt for it.
First, ask me for everything you need: audience, context, format, length, tone and anything that must not appear.
Then give me the finished prompt as a block I can copy, and explain in three bullet points why it is built that way.
```

```
Here is my prompt: [paste prompt].
Assess it on six points: role, goal, context, material, format, constraints.
For each point, say what is missing or ambiguous.
Then give me an improved version without changing my content requirements.
```

## Tips and tricks
- **Outline first, then the text**: Ask to see the structure first and approve it. The wrong structure costs more time than any wording.
- **Say what you want, not just what you don't**: Bans alone produce bland results. One example of the tone you want works better than five bans.
- **Ask for criticism, not agreement**: Models agree too readily. Ask explicitly: "What are the arguments against this?" or "Where is the text weak?"
- **Have gaps flagged**: Ask the model to mark anything uncertain, for example with [OPEN] or [SOURCE?]. That separates what is known from what is guessed before you use it.
- **Restart long conversations**: After many rounds, answers drift. Have the current state summarised and start again with that summary.
- **Two options, not one**: Ask for two different solutions, each with a one-sentence rationale. Comparing is easier than judging.

## Build it once, use it every time
- Once a task has gone well, don't save the prompt in a document; save the procedure in the tool itself.

```
That worked well. Summarise the procedure we just used as a reusable workflow:
what role you take on, what information you need from me, the order you work in and how you check the result.
Write it so I can save it and call it up with one sentence next time.
Call the workflow [name].
```