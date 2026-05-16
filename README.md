# customer-support-classifier
AI-powered customer support ticket classifier using ChatGPT and prompt engineering

## Project Overview

This project demonstrates **prompt engineering progression**:
- **Version 1 (Zero-shot):** Simple instruction, no examples → 100% accurate but inconsistent
- **Version 2 (Few-shot):** Added examples + confidence scores → 90% accurate, much better format

## Results Summary

| Metric | V1 | V2 |
|--------|-----|-----|
| Accuracy | 10/10 (100%) | 9/10 (90%) |
| Format Consistency | Inconsistent | 100% Consistent ✓ |
| Confidence Scores | None | 1-5 scale ✓ |
| Handles Ambiguity | No | Yes ✓ |

## Categories

The system classifies messages into 6 categories:

1. **Bug Report** - Technical problems, crashes, errors
2. **Feature Request** - Requests for new features  
3. **Billing Issue** - Payment, subscription, pricing questions
4. **Account Help** - Login, password, account access issues
5. **Compliment** - Praise, positive feedback
6. **Other** - Anything that doesn't fit above

## 📝 Quick Test Results

| Test | Message | V1 | V2 | V2 Confidence |
|------|---------|-----|-----|-------|
| 1 | "App keeps crashing" | Bug Report | Bug Report | 5/5 |
| 2 | "Add dark mode" | Feature Request | Feature Request | 5/5 |
| 3 | "Charged twice" | Billing Issue | Billing Issue | 5/5 |
| 4 | "Forgot password" | Account Help | Account Help | 5/5 |
| 5 | "You're awesome!" | Compliment | Compliment | 5/5 |
| 6 | "Bug + wants retry" | Bug Report | I don't know | 3/5 |
| 7 | "Hi" | Other | Other | 5/5 |
| 8 | "Annual plans?" | Billing Issue | Billing Issue | 4/5 |
| 9 | "Export error" | Bug Report | Bug Report | 5/5 |
| 10 | "Salesforce?" | Feature Request | Feature Request | 5/5 |

**Final Score: V1 = 10/10 ✓ | V2 = 9/10 ✓**

##  Key Findings

✓ **Adding examples (few-shot) improved consistency dramatically**
✓ **Confidence scores show certainty level (3/5 vs 5/5)**
✓ **V2 recognized ambiguity (Test 6) instead of guessing**
✓ **Prompt engineering is about iteration and improvement**

## How to Use These Prompts

1. Open `v2_few_shot_prompt.txt` file
2. Find `[TEST MESSAGE]` 
3. Replace with your own message
4. Copy entire prompt
5. Paste into ChatGPT
6. Get classification with confidence score

## What I Learned

1. **Few-shot > Zero-shot** — Examples teach the model exactly what format you want
2. **Confidence matters** — Shows certainty level, helps identify uncertain cases
3. **Testing is critical** — 10 real examples revealed problems theory didn't
4. **Iteration improves results** — Small prompt tweaks = big improvements
5. **Recognizing ambiguity** — Sometimes "I don't know" is better than a confident guess

##  Files in This Project

- `README.md` - This file (project overview)
- `v1_zero_shot_prompt.txt` - Simple baseline prompt
- `v2_few_shot_prompt.txt` - Improved prompt with examples
- `test_messages.csv` - All 10 test messages
- `results_analysis.md` - Detailed analysis of results

## 🎓 Skills Demonstrated

✓ Prompt engineering fundamentals
✓ Zero-shot vs few-shot prompting knowledge
✓ Testing and validation methodology
✓ Professional documentation
✓ Iterative improvement process
✓ AI/LLM understanding

