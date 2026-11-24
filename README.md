# PlanFlow

PlanFlow generates a personalised, day-wise study timetable from subjects, difficulty levels, exam dates, daily study hours, preferred study time and break rules. It respects time limits, gives more time to harder subjects, adds breaks, and plans a revision day before each exam.

## Team Neural Nomads
- Angela Gupta (S24CSEU2551)
- Priyal Shrivastava (S24CSEU2582)

## Tool
Gemini 4 Hydrogen (`gemini-4-hydrogen`) in Google AI Studio

## Prototype
<PASTE PROTOTYPE LINK HERE>

## How to use
1. Open the prototype link.
2. Enter subjects with difficulty, exam dates, start date, daily study hours, preferred study time and break rule.
3. The app returns a day-wise timetable as a table.

To test the prompt directly: open Google AI Studio Playground, paste `prompts/final/P1_timetable_generator_v3_system.txt` into System instructions, then paste the user template from `prompts/final/P1_timetable_generator_v3_user.txt` with the variables filled in.

## Folder guide
- `prompts/v1/` : baseline prompt
- `prompts/v2/` : constraint-based prompt
- `prompts/final/` : final prompt (v3: system prompt + user template)
- `test-data/` : test inputs and results sheets
- `code/` : prototype code or exported app
- `docs/` : prompt iteration log, diagrams and the Milestone 2 PDF
- `CHANGELOG.md` : dated changes since Milestone 1
