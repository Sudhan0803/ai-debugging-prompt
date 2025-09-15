# ai-debugging-prompt
# Python Screening Task 2: AI Debugging Assistant Prompt

This repository contains my submission for the screening task to create a prompt for an AI Debugging Assistant.

## Contents
- `PROMPT.md`: The main prompt for the AI assistant.
- `README.md`: This file, containing the reasoning and setup instructions.

## The Prompt
The prompt is designed to instruct an AI model (like ChatGPT) to act as a helpful debugging mentor for students learning Python. Its core principle is to **guide without giving away the solution**.

Find the full prompt in [PROMPT.md](./PROMPT.md).

## Reasoning and Design Choices

### 1. Why you worded it the way you did
*   **Role-Playing (`CodeMentorAI`)**: Starting with a role primes the AI to adopt a specific persona, which is more effective than a dry list of instructions. It sets a consistent, supportive tone.
*   **Structured Steps (Analyze, Engage, Guide, Encourage)**: This provides a clear, repeatable framework for the AI to follow for any piece of code it receives, ensuring consistency in its approach.
*   **Explicit "DO" and "DO NOT" Rules**: AI models benefit from very clear, unambiguous boundaries. By explicitly forbidding certain actions (providing full code) and mandating others (asking questions), the prompt reduces the chance of the AI accidentally revealing the solution.
*   **Concrete Examples**: Including examples of both good and bad hints gives the AI a tangible reference for the style and depth of feedback required.

### 2. How you ensured it avoids giving the solution
The prompt employs a multi-layered strategy to prevent solution revelation:
*   **Direct Prohibition:** It explicitly commands the AI to "NEVER provide the corrected, full code block" and "NEVER simply state the exact line number and the fix."
*   **Redirection via Questions:** The core instruction is to "ask a targeted, leading question." This forces the AI to engage the student's problem-solving skills instead of just providing an answer.
*   **Symptom Description vs. Solution Description:** The AI is instructed to describe the *effect* of the bug rather than its *cause and fix*. This points the student in the right direction without handing them the answer.

### 3. How it encourages helpful, student-friendly feedback
*   **Positive Framing:** Instructions like "Frame your hints positively" ensure the AI's tone is constructive and builds confidence.
*   **Metacognition:** The initial step to "Engage" the student prompts them to think about their own logic, a crucial debugging skill.
*   **Empowerment:** The prompt guides the AI to give the student actionable next steps, empowering them to investigate independently.

## Answers to Reasoning Questions

**What tone and style should the AI use when responding?**
The AI should adopt the tone of a **patient, encouraging, and knowledgeable tutor**. The style should be supportive, clear, Socratic (asking questions), and collaborative.

**How should the AI balance between identifying bugs and guiding the student?**
The balance should be 20% identification and 80% guidance. The AI's primary job is not to just be a bug-finder but to be a teacher. It should identify the bug internally but guide the student externally through questions and suggestions for discovery.

**How would you adapt this prompt for beginner vs. advanced learners?**
*   **For Beginners:** Add instructions to use simpler language, explain fundamental concepts, and suggest very concrete debugging steps (e.g., "use print statements here").
*   **For Advanced Learners:** Add instructions that allow for more technical terminology and conceptual hints about algorithm efficiency or design patterns.

## How to Use / Setup
This prompt is ready to be copied and pasted into any AI chat interface (OpenAI ChatGPT, Claude, etc.) as a system prompt or initial user message. The AI will then be primed to debug code according to the specified guidelines.
