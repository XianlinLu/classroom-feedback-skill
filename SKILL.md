---
name: classroom-feedback-skill
description: Write concise Chinese, parent-facing feedback from a classroom or lesson screenshot. Use when the user uploads a course interface, textbook page, lesson summary, or student-class screenshot and asks “帮我给图中的小朋友写一个点评” or makes an equivalent request for a child’s lesson feedback.
---

# Classroom Feedback Skill

Turn the screenshot and any accompanying teacher notes into a polished Chinese classroom comment that can be sent directly to a parent.

## Read the evidence

1. Inspect the screenshot for the lesson title, overview, topic, target vocabulary, sentence patterns, grammar, phonics, reading content, and visible student name.
2. Treat the user’s written notes as authoritative, especially comments about participation, pronunciation, comprehension, attention, confidence, or homework.
3. Ignore administrative details such as lesson IDs, dates, class times, account numbers, and generic labels such as `Unknown`.
4. If no real student name is visible, use “宝贝”. Never call the child “Unknown”.

## Evidence boundaries

- Ground the learning content and knowledge summary in the screenshot. Do not invent lesson details that are not visible or strongly supported by the title and overview.
- When only a broad topic is visible, describe broad categories such as “玩具类词汇” instead of claiming that specific words appeared.
- User-provided performance notes may support specific praise or improvement advice. When performance evidence is absent, use restrained language such as “整体能够跟随老师的引导参与课堂”; do not claim unusually high accuracy, strong concentration, frequent independent answers, or specific pronunciation errors.
- Do not ask a follow-up question when a useful comment can be written from the available material.

## Required output structure

Write in this order:

1. **What the child learned and how the teacher guided them** — one natural paragraph. State the lesson topic, vocabulary or content, the main sentence pattern or language point, and the teacher’s use of pictures, questions, demonstrations, reading prompts, or sentence-building practice.
2. **Performance and improvement** — one natural paragraph. Give balanced, encouraging feedback, then one or two concrete next steps. Keep praise measured and avoid negative labels.
3. **知识点梳理：** — a short bullet list covering only applicable items:
   - 主题词汇或阅读主题
   - 核心句型或语法结构
   - One or two short English examples
   - A question-and-answer pattern when relevant
   - One useful grammar, pronunciation, phonics, or reading reminder

## Writing style

- Write the final answer in natural Simplified Chinese, with English words and example sentences where useful.
- Address the child as the visible name or “宝贝”. Use a warm, professional, parent-facing tone.
- Keep the response concise but informative, normally two paragraphs followed by the knowledge summary.
- Integrate the four requested dimensions smoothly rather than using separate headings for each one. Use only “知识点梳理：” as a visible section label.
- Prefer specific teaching actions such as “老师通过图片观察和提问，引导宝贝使用完整句子回答” over vague claims.
- Phrase improvement points constructively, for example “接下来可以更加大胆、主动地开口” or “可以减少只回答单个单词的情况”.
- Avoid excessive praise, emojis, scores, and unsupported comparisons with previous lessons.

## Example shape

For a lesson titled *I Want Toys*, a suitable response should resemble this structure while adapting every detail to the actual screenshot:

> 宝贝今天学习了“I Want Toys”主题课程，认识并复习了玩具类英文表达，重点练习了用“I want a…”表达自己想要的玩具。课堂中，老师通过图片观察、提问和句型示范，引导宝贝辨认玩具，并尝试用完整句子表达自己的想法。
>
> 宝贝整体能够跟随老师的节奏参与课堂，在图片提示下逐步练习目标表达。接下来可以更加大胆、主动地开口，减少只回答单个单词的情况，并继续加强词汇发音和记忆。课后可以结合身边物品重复练习核心句型。
>
> 知识点梳理：
>
> - 主题词汇：玩具类单词
> - 核心句型：**I want a + 玩具名称.**
> - 示例：**I want a ball.**
> - 问答练习：**What do you want? — I want a…**
> - 语法提醒：可数名词单数前通常需要使用 **a**。

Use the example as a structural reference, not as reusable lesson content.
