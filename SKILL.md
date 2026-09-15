---
name: classroom-feedback-skill
description: Write concise Chinese, parent-facing feedback from a classroom or lesson screenshot, including regular lessons and placement lessons whose title contains DEMO. Use when the user uploads a course interface, textbook page, lesson summary, or student-class screenshot and asks “帮我给图中的小朋友写一个点评” or makes an equivalent request for a child’s lesson feedback.
---

# Classroom Feedback Skill

Turn the screenshot and any accompanying teacher notes into a polished Chinese classroom comment that can be sent directly to a parent.

## Read the evidence

1. Inspect the screenshot for the lesson title, overview, topic, target vocabulary, sentence patterns, grammar, phonics, reading content, and visible student name.
2. Treat the user’s written notes as authoritative, especially comments about participation, pronunciation, comprehension, attention, confidence, or homework.
3. Ignore administrative details such as lesson IDs, dates, class times, account numbers, and generic labels such as `Unknown`.
4. If no real student name is visible, use “宝贝”. Never call the child “Unknown”.

## Classify the lesson

Use the lesson title as the only placement-lesson trigger:

- If the screenshot's lesson title contains the exact text `DEMO`, treat it as a placement lesson.
- Otherwise, treat it as a regular lesson. Do not infer a placement lesson from words such as “体验课”, “试听课”, “测评”, or from the page design alone.
- Check the title before choosing the output structure.

## Evidence boundaries

- Ground the learning content and knowledge summary in the screenshot. Do not invent lesson details that are not visible or strongly supported by the title and overview.
- When only a broad topic is visible, describe broad categories such as “玩具类词汇” instead of claiming that specific words appeared.
- User-provided performance notes may support specific praise or improvement advice. When performance evidence is absent, use restrained language such as “整体能够跟随老师的引导参与课堂”; do not claim unusually high accuracy, strong concentration, frequent independent answers, or specific pronunciation errors.
- Do not ask a follow-up question when a useful comment can be written from the available material.

## Classroom state is required

Every regular lesson and placement lesson must tell the parent what the child's classroom state was like. Do not replace this with a vague sentence such as “今天表现不错”.

- Select two or three relevant dimensions when supported: willingness to answer, response speed, speaking confidence, focus, ability to return to the task after a reminder, independent thinking, reliance on teacher prompts, participation in reading or repetition, and completion of classroom tasks.
- Describe observable behaviour and the level of support needed. Useful patterns include “在图片提示下能够说出目标词汇”, “回答完整句时需要老师给出句型开头”, and “个别环节需要老师点名或再次提问后回到课堂”.
- State both a positive aspect and one realistic area for improvement. Do not hide a classroom-state issue behind general praise.
- Connect the state to the teacher's response. Explain what the teacher did after noticing hesitation, distraction, single-word answers, pronunciation difficulty, or uncertainty, and whether the child could continue after that guidance.
- If the user supplies no classroom-state notes and the screenshot contains none, remain cautious. Describe only that the child completed the main activities with teacher guidance and identify the degree of prompting needed for the target task. Do not invent detailed claims about concentration, accuracy, mood, or independent performance.
- Use constructive wording. For intermittent attention, write “课堂投入度有所提升，个别环节需要老师点名或再次提问后回到任务”, not “注意力不集中”.

## Regular lesson structure

For a regular lesson, write in this order:

1. **What the child learned and how the teacher guided them** — one natural paragraph. State the lesson topic, vocabulary or content, the main sentence pattern or language point, and the teacher’s use of pictures, questions, demonstrations, reading prompts, or sentence-building practice.
2. **Classroom state, performance, and improvement** — one natural paragraph. Clearly describe how the child participated, responded, stayed with the lesson, and used teacher support. Give one positive observation and one or two concrete next steps. Keep praise measured and avoid negative labels.
3. **知识点梳理：** — a short bullet list covering only applicable items:
   - 主题词汇或阅读主题
   - 核心句型或语法结构
   - One or two short English examples
   - A question-and-answer pattern when relevant
   - One useful grammar, pronunciation, phonics, or reading reminder

## Placement lesson structure

For a placement lesson, do not use the regular lesson structure. Write in this order:

1. Begin with `推荐级别：` followed by exactly one level, such as `推荐级别：F`.
2. Describe the child's classroom state and what they did well, using evidence from the screenshot and teacher notes. Make participation, response behaviour, confidence, focus, or reliance on prompts clear to the parent.
3. Explain what needs improvement in constructive language. Focus on one or two priorities such as speaking in complete sentences, answering independently, pronunciation, reading comprehension, or confidence.
4. Give more space to the teacher's concrete guidance. State what content, sentence pattern, grammar point, pronunciation feature, reading strategy, or response method the teacher taught and how the teacher prompted the child to practise it.
5. Finish with specific after-class actions, such as reviewing the lesson recording, memorising the lesson vocabulary, shadow-reading, correcting target sounds, or practising complete-sentence answers.

Prefer a visible recommended level from the screenshot. If no recommendation is displayed, select one level from the visible course band using the lesson difficulty and the user's performance notes. Do not output a level range.

## Writing style

- Write the final answer in natural Simplified Chinese, with English words and example sentences where useful.
- Address the child as the visible name or “宝贝”. Use a warm, professional, parent-facing tone.
- Keep the entire feedback within 500 Chinese characters, including the recommended level and knowledge summary. Aim for 300 to 450 Chinese characters when the evidence supports enough detail.
- Never use an em dash or en dash in the final feedback. Do not use `—` or `–`. Join ideas with commas, colons, semicolons, or full stops instead.
- Remove formulaic AI phrasing. Write like a teacher reporting a lesson they personally taught. Use concrete observations and teaching actions, vary sentence length naturally, and avoid empty phrases such as “总体而言”, “值得肯定”, or repeated generic praise.
- For regular lessons, integrate the requested dimensions smoothly rather than using separate headings for each one. Use only “知识点梳理：” as a visible section label.
- For placement lessons, use only `推荐级别：` as a required label. The remaining content should read as a natural teacher comment rather than a form or scorecard.
- Prefer specific teaching actions such as “老师通过图片观察和提问，引导宝贝使用完整句子回答” over vague claims.
- Pair each classroom-state observation with a concrete behaviour. Prefer “老师提问后能够及时回应，遇到长句时需要分段提示” over “课堂状态良好”.
- Phrase improvement points constructively, for example “接下来可以更加大胆、主动地开口” or “可以减少只回答单个单词的情况”.
- Avoid excessive praise, emojis, scores, and unsupported comparisons with previous lessons.
- Before sending, check the lesson mode, level format when applicable, 500-character limit, and absence of forbidden dash punctuation.

## Example shape

For a lesson titled *I Want Toys*, a suitable response should resemble this structure while adapting every detail to the actual screenshot:

> 宝贝今天学习了“I Want Toys”主题课程，认识并复习了玩具类英文表达，重点练习了用“I want a…”表达自己想要的玩具。课堂中，老师通过图片观察、提问和句型示范，引导宝贝辨认玩具，并尝试用完整句子表达自己的想法。
>
> 课堂中，宝贝能够在图片提示下辨认玩具并完成跟读，回答问题的意愿不错。遇到需要完整句子表达的问题时，偶尔会先说单个词，在老师给出句型开头后能够继续补充。接下来可以更加大胆、主动地开口，减少只回答单个单词的情况，并继续加强词汇发音和记忆。课后可以结合身边物品重复练习核心句型。
>
> 知识点梳理：
>
> - 主题词汇：玩具类单词
> - 核心句型：**I want a + 玩具名称.**
> - 示例：**I want a ball.**
> - 问答练习：**What do you want? I want a…**
> - 语法提醒：可数名词单数前通常需要使用 **a**。

Use the example as a structural reference, not as reusable lesson content.

For a placement lesson whose title contains `DEMO`, use this shape while adapting every detail to the evidence:

> 推荐级别：F
>
> 从今天的定级课来看，宝贝的基础词汇掌握较扎实，能够听懂主要指令并积极参与跟读，绘本理解也比较顺畅。回答事实类问题时反应较快，遇到开放性问题时会先用单词作答，需要老师追问后才能补充完整句子。课堂中，老师结合图片和故事情节，引导宝贝定位关键信息，示范目标句型，再通过分步提问帮助宝贝组织表达。课后建议复习本节课的生词，跟读课堂录音，重点练习老师纠正过的发音和句型，并尝试用完整句子回答相关问题。
