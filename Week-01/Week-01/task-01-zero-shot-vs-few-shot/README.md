# Task: Zero-Shot vs Few-Shot Prompting Showdown

## 📋 Task Overview

**Objective:** Compare zero-shot vs few-shot prompting for classifying customer support messages.

**Tools Used:** ChatGPT, Claude, Gemini

**Date Completed:** February 2026

---

## 📝 The 10 Customer Support Messages

| # | Message | True Label |
|:---|:---|:---:|
| 1 | "I am extremely disappointed with the product. It broke after two days." | Complaint |
| 2 | "How do I reset my password? I can't find the option." | Question |
| 3 | "Amazing service! The team was super helpful and quick." | Praise |
| 4 | "My order hasn't arrived yet. It's been a week." | Complaint |
| 5 | "Can you tell me the return policy for electronics?" | Question |
| 6 | "I love your new feature. It's so intuitive." | Praise |
| 7 | "The app keeps crashing every time I open it. This is frustrating." | Complaint |
| 8 | "What are your business hours on weekends?" | Question |
| 9 | "Your customer support team is the best I've ever dealt with." | Praise |
| 10 | "I received a damaged item. I want a refund." | Complaint |

---

## 🔬 Zero-Shot Prompt (No Examples)
Classify the following customer support messages as "Complaint", "Question", or "Praise".
Only output the label for each message, one per line in order.

"I am extremely disappointed with the product. It broke after two days."

"How do I reset my password? I can't find the option."

"Amazing service! The team was super helpful and quick."

"My order hasn't arrived yet. It's been a week."

"Can you tell me the return policy for electronics?"

"I love your new feature. It's so intuitive."

"The app keeps crashing every time I open it. This is frustrating."

"What are your business hours on weekends?"

"Your customer support team is the best I've ever dealt with."

"I received a damaged item. I want a refund."


---

## 🔬 Few-Shot Prompt (Instruction + 3 Examples)
Classify the following customer support messages as "Complaint", "Question", or "Praise".
Here are three examples:

Message: "I am very unhappy with the delay." Label: Complaint
Message: "When will my order ship?" Label: Question
Message: "Thank you for the excellent support." Label: Praise

Now classify the messages below. Output only the label for each message, one per line.

"I am extremely disappointed with the product. It broke after two days."

"How do I reset my password? I can't find the option."

"Amazing service! The team was super helpful and quick."

"My order hasn't arrived yet. It's been a week."

"Can you tell me the return policy for electronics?"

"I love your new feature. It's so intuitive."

"The app keeps crashing every time I open it. This is frustrating."

"What are your business hours on weekends?"

"Your customer support team is the best I've ever dealt with."

"I received a damaged item. I want a refund."


---

## 📊 Accuracy Results

| **Tool** | **Zero-Shot** | **Few-Shot** |
|:---|:---:|:---:|
| **ChatGPT** | 10/10 ✅ | 10/10 ✅ |
| **Claude** | 10/10 ✅ | 10/10 ✅ |
| **Gemini** | 9/10 | 10/10 ✅ |

---

## 📈 Analysis

The few-shot approach achieved perfect accuracy across all three tools, while zero-shot performance varied and was noticeably lower. 

**Key Insights:**
1. **Examples improve accuracy** - Providing examples anchors the model's understanding
2. **Models vary in zero-shot** - ChatGPT and Claude performed perfectly, Gemini struggled slightly
3. **Few-shot is more reliable** - Perfect accuracy across all tools with examples

**Why Few-Shot Works Better:**
Providing examples explicitly anchors the model's understanding of the task's boundaries, especially subtle distinctions like a frustrated statement that is still a complaint vs. a polite inquiry. Without examples, the model relies on its prior training, which can lead to inconsistent interpretation of tone and intent.

---

## 💡 Conclusion

Even a small number of well-chosen examples dramatically improve reliability and reduce ambiguity in classification tasks. Few-shot prompting is clearly the superior approach for this use case.

---

## 📎 Attachments

- 📄 `Task-01_Zeroshot and FewShot_prompt.docx` - Original task document

---

*Task completed on: 26 July, 2026*
