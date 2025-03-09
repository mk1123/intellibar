Given the following document:

<text>
{selection}
</text>

And the following hastily written intent of mine of reading this document:

<text>
{argument}
</text>

First, rewrite my shorthand intent ({{ intent }}) to be clearer, beginning your response with Background: followed by the clearer intent.

Then, summarize the three most important takeaways that stood out to me according to my intent. If a takeaway is common knowledge or not worth remembering, do not include it. A takeaway does not need to be a key insight, but it could also be a unique term, definition, or any component of the document worth remembering. Make sure to include at least three takeaways, but feel free to add more, depending on the length of the document. 

Then, use the spaced repetition guidelines below to generate spaced repetition prompts given the list of takeaways. Use the number of paragraphs in the document as a rough heuristic for the number of spaced repetition prompts to generate; i.e., if there are three paragraphs in the document, generate three prompts. Gravitate towards outputting less prompts than necessary rather than more, especially if the document is shorter than 3 or 4 paragraphs.

<principles>
Spaced repetition prompts should be focused. A question or answer involving too much detail will dull your concentration and stimulate incomplete retrievals, leaving some bulbs unlit. Unfocused questions also make it harder to check whether you remembered all parts of the answer and to note places where you differed. It’s usually best to focus on one detail at a time.

Spaced repetition prompts should be precise about what they’re asking for. Vague questions will elicit vague answers, which won’t reliably light the bulbs you’re targeting.

Spaced repetition prompts should produce consistent answers, lighting the same bulbs each time you perform the task. Otherwise, you may run afoul of an interference phenomenon called "retrieval-induced forgetting": what you remember during practice is reinforced, but other related knowledge which you didn't recall is actually inhibited. Now, there is a useful type of prompt which involves generating new answers with each repetition, but such prompts leverage a different theory of change. We'll discuss them briefly later in this guide.

Spaced repetition prompts should be tractable. To avoid interference-driven churn and recurring annoyance in your review sessions, you should strive to write prompts which you can almost always answer correctly. This often means breaking the task down, or adding cues.
Spaced repetition prompts should be effortful. It's important that the prompt actually involves retrieving the answer from memory. You shouldn't be able to trivially infer the answer. Cues are helpful, as we'll discuss later—just don't "give the answer away." In fact, effort appears to be an important factor in the effects of retrieval practice. That's one motivation for spacing reviews out over time: if it's too easy to recall the answer, retrieval practice has little effect.
</principles>

Also keep the following spaced repetition rules in mind as well.

<rules>
Rule: Repeat Yourself
Memory is frequency times volume. Individual cards should be extremely brief, but your deck as a whole can be as repetitive as you want.

Rule: Write Atomic Flashcards
Cards should be short. They should refer to as little information as possible. They should be like chemical bonds, linking individual atoms of knowledge.

This is the most important thing. By far the worst failure mode is to put too much in a flashcard.

There’s two reasons for this rule:

Larger cards are harder to remember.
It’s harder to objectively grade yourself: when you reveal the answer, you might have got some things right and some things wrong. If you click forget, you will be over-reviewing the parts you already know. If you click remembered, you will under-review the parts you forgot.
There is one exception to this: you can have big cards if you also have smaller cards that add up to the same information. You can think of the larger card as testing that you can collate the information from the smaller cards.

Rule: Write Two-Way Questions
When possible, ask questions in two directions.

Whenever you have a term with a definition, the obvious thing to do is to ask for the definition from the term, e.g.:

Q: What is the order of a group?

A: The cardinality of its underlying set.

But you can also ask for the term from the definition, e.g.:

Q: What is the term for the cardinality of a group?

A: The group’s order.

Rule: Ask Questions in Multiple Ways
Ask questions in multiple ways. Ask for formal and informal definitions of terms. Ask for the formal and informal statements of a theorem. Ask questions forwards and backwards. Add contextual questions: “what is the intutition for [concept]?”. Add questions that link different concepts across your knowledge graph.


Rule: Cache Your Insights
When studying, you will often infer new knowledge that is not explicitly written down in the text by thinking about what you’ve just read. After verifying that your inference is actually true, it can be helpful to “cache your insight”—to make a flashcard for that new discovered piece of knowledge.

Rule: Learning Hierarchies
A lot of knowledge is hierarchical, of the form “Foo can be either A, B, or C”, or, dually, “A is a kind of Foo”. By analogy to OOP: these concepts are joined by superclass and subclass relations.

The idea is to ask questons in the top down direction (“What are the subclasses of Foo?”) and the bottom-up direction (“What is Bar a subclass of?”).

This ties into keeping flashcards atomic. Even when some information is not hierarchical, intrinsically, breaking down large flashcards into smaller flashcards is fundamentally building a hierarchy of flashcards.
</rules>

Here are some examples of the types of prompts that I want you to generate:

<example>
What is the Castner-Kellner process?

***

Method of electrolysis, takes an alkali chloride to produce the corresponding alkali hydroxide. 
</example>
<example>
Who wrote Mother Courage and Her Children?

***

Bertolt Brecht
</example>

Ensure that all of the prompts are standalone; I should be able to read the question of the prompt and have all the context that I need to provide an answer.  All of the prompts should assess my understanding of a particular takeaway of the text.

As a reminder, ensure that all of the generated flashcards follow the rules of spaced repetition as much as possible:

1. Repeat yourself
2. Write atomic flashcards
3. Write two-way questions
4. Ask questions in multiple ways
5. Cache your insights
6. Learning hierarchies

First, output the list of key takeaways. Then, output the list of flashcards in descending order of how important they are to remember about the document, given my intent and the key takeaways. 

The number one most important rule to remember in your output: The flashcards should be short and contain as little information as possible.

Do not output anything else. Make sure to output the flashcards in the exact format I specified above, separated with a new line:

<example>
Who wrote Mother Courage and Her Children?
---
Bertolt Brecht
</example>