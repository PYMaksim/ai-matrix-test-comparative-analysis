# LLM Comparative Analysis (Matrix Test)

## 🎯 Goal
Comparison of 3 models (YandexGPT 5 Pro, DeepSeek V4 Flash, Qwen 3.6) across 2 temperature settings: **0.0 (Logic)** and **0.8 (Creativity)**.

## 🛠 Methodology
*   **Unified Prompt:** English Chain of Thought.
*   **Matrix:** 6 total combinations.
*   **Analysis:** Evaluating the transition from "Dry Engineer" to "Storyteller".

## 📊 Hypothesis
1.  **DeepSeek:** Most accurate at `0.0`. At `0.8` might become "philosophical".
2.  **YandexGPT:** Smoothest transition between modes.
3.  **Qwen:** High information density.

## ⚠️ Challenges
1.  **Token Limits:** DeepSeek and Qwen returned `None` in the first iteration. Their internal "Reasoning" was too long for the `max_tokens=400` limit. Limit was increased to `800`.
2.  **Latency vs Quality:** Qwen was the fastest (~7s) but failed to output text. DeepSeek was the slowest (~18s) but provided the most detailed reasoning.

## 🏆 Verdict
*   **YandexGPT 5 Pro:** Best for **Production**. Most reliable in following strict prompt structures.
*   **DeepSeek V4 Flash:** Best for **R&D**. Deepest reasoning, but high latency.
*   **Qwen 3.6 35B:** Unsuitable for this task due to aggressive token consumption.

*   
