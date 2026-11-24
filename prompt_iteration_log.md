# Prompt iteration log (PlanFlow)

Model: Gemini 4 Hydrogen in Google AI Studio Playground. Settings for all versions: Thinking level High, Grounding with Google Search OFF, all other tools OFF, temperature at default (not adjustable for this model in AI Studio). Each version was run 5 times, each run in a new chat, with the same input.

| Version | What changed | Why it was changed | Result after the change |
|---|---|---|---|
| v1 | Baseline prompt: subjects, 4 hrs/day, exam order, columns Day, Time, Subject, Task | Starting point | 5 runs: 4-hr daily limit kept 5/5; Maths got most time 5/5; separate 10-minute break rows 0/5 (a gap between blocks in 4/5); revision included in 2/5 fully and 3/5 partly; real dates 0/5 (only Day 1-7 or Mon-Sun); table-only format 0/5 (intro text or summary list every time); output layout and time slots changed from run to run |
| v2 | Added difficulty levels, exam dates, start date, preferred time, break rule, 6 rules, and the Duration column | v1 had no dates or breaks and the layout changed every run | 5 runs: hours limit 5/5; 10-minute break rows 5/5; Hard subject most time 5/5; revision day before each exam 5/5; real dates 5/5; inside 6-11 PM window 5/5; table-only format still 0/5 (intro, summary list, or extra "Exam Day" rows every time) |
| v3 | Added a system prompt (PlanFlow role and invalid-input reply), strict "ONLY a Markdown table" output rule, 2 worked examples and a same-date exam rule | v2 still added extra text and Exam Day rows around the table | 5 runs: hours limit 5/5; break rows 5/5; Hard subject most time 5/5; revision day before each exam 5/5; real dates 5/5; inside 6-11 PM window 5/5; table-only format 5/5. Remaining weakness: in 2/5 runs the revision rows only said "Revision (exam tomorrow)" without a topic, and the daily total came as the last table row instead of a separate line |

## Full prompt text
The full text of each version is saved in:
- prompts/v1/v1_prompt.txt
- prompts/v2/v2_prompt.txt
- prompts/final/P1_timetable_generator_v3_system.txt and P1_timetable_generator_v3_user.txt
