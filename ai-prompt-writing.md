# A Practical Guide to AI Prompt Writing

**Author: Paul Kato**

## Purpose

A strong prompt gives an AI system enough context to produce a useful result, while making the requested outcome easy to recognize. Prompt writing is an iterative practice: describe the task, inspect the response, and refine the instructions based on what did or did not work.

## The essential parts of a prompt

1. **Goal** — State the task and the result you need.
2. **Context** — Provide the facts, audience, and situation the model needs. Include source material when accuracy depends on it.
3. **Instructions** — Specify the actions to take, the order of work, and any limits.
4. **Output shape** — Name the format, length, structure, tone, or fields expected.
5. **Quality criteria** — Explain what a successful answer must include or avoid.
6. **Uncertainty handling** — Tell the model how to handle missing, conflicting, or unsupported information.

Not every prompt needs a heading for each part. The point is to make the task and expectations explicit.

## A reusable prompt pattern

> **Task:** [What should be done?]
>
> **Context:** [Who is this for, and what background or source material matters?]
>
> **Instructions:** [What steps should the model follow?]
>
> **Requirements:** [What must the answer include? What constraints apply?]
>
> **Output:** [Format, length, tone, and organization.]
>
> **If information is missing:** [Ask a question, state an assumption, or mark the gap.]

## Write instructions that can be followed

- Use concrete verbs such as *summarize*, *compare*, *classify*, or *draft*.
- Separate required content from optional suggestions.
- Define ambiguous terms, audiences, and time ranges.
- Put the most important constraints near the task.
- Supply examples when they clarify the desired result. Label examples as examples so they are not mistaken for source facts.
- For multi-step work, number the steps and state which output each step should produce.
- Ask for a concise explanation or evidence when it helps review the answer. Avoid requesting hidden reasoning; request conclusions, assumptions, and supporting evidence instead.

## Ground answers in provided material

When the task depends on a source, name it and state how to use it. For example: “Use only the supplied policy excerpt. If it does not answer a question, say ‘Not specified in the excerpt.’” This reduces unsupported additions and makes gaps visible.

If sources may conflict, specify which source takes precedence or ask the model to flag the conflict. For factual or high-stakes work, verify important claims against authoritative sources and use an appropriate human reviewer.

## Improve a prompt through iteration

1. Run the prompt on representative examples.
2. Compare the output with the intended result.
3. Identify the precise failure: missing context, ambiguous instruction, unsuitable format, or weak quality criterion.
4. Change the smallest relevant part of the prompt.
5. Try the revised prompt on both typical and edge cases.
6. Keep examples of successful and unsuccessful outputs so future changes can be evaluated consistently.

Avoid adding broad instructions such as “be better” when a specific correction is possible. Replace them with observable requirements.

## Example: vague request to usable prompt

**Vague:** “Write something about our product.”

**More usable:**

> Write a welcome email for people who registered for the free “Getting Started with Composting” workshop at Northside Public Library. The workshop is on Saturday, April 18, from 10:00 to 11:30 a.m., in the library’s Community Room at 24 Maple Street. Attendees should bring a notebook; all workshop materials are provided. The room is wheelchair accessible. Ask attendees to reply to the email if they need to cancel so someone on the waitlist can take their place.
>
> Keep the email between 120 and 160 words, use a warm and practical tone, and include a subject line. Do not add claims about what attendees will learn beyond the workshop title, or invent parking, transit, or contact details.

## Common failure patterns

- **Missing context:** Provide the audience, purpose, and relevant source information.
- **Conflicting instructions:** Remove contradictions and order requirements by priority.
- **Unclear scope:** State what is in and out of scope.
- **Wrong level of detail:** Set a word range or list the sections expected.
- **Invented facts:** Restrict sources and define what to do when evidence is absent.
- **Inconsistent results:** Add a rubric, examples, or a structured output schema.
- **Prompt overloading:** Remove instructions that do not affect the outcome; split unrelated tasks when useful.

## Prompt review checklist

- Is the requested task clear and achievable?
- Does the prompt provide the necessary context and source material?
- Are constraints, priorities, and exclusions explicit?
- Is the intended audience identified?
- Is the output format reviewable?
- Does the prompt explain how to handle uncertainty or missing evidence?
- Can a reviewer tell whether the answer meets the stated criteria?
- Have representative and edge cases been tried?

## Responsible use

Do not include confidential or personal information unless the tool and workflow are approved for it. Check generated material before relying on it, especially when it affects people, safety, legal obligations, finances, or access to services. Follow applicable organizational policies and disclose AI assistance when required.
