# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").

When I first ran the game, it looked functional on the surface but behaved
incorrectly during play. The hints were backwards — when my guess was too
high, the game told me to go higher instead of lower, which made it
impossible to win logically. When I clicked "New Game", the game did not
properly restart; the score and status carried over from the previous game.
These bugs were subtle enough that the app still ran without crashing,
which made them harder to spot at first.

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).

---

I used GitHub Copilot (Chat and Inline Chat) throughout this project.

**Correct suggestion:**
Copilot correctly identified that the hint messages were swapped.
"Too High" was showing "Go HIGHER!" when it should say "Go LOWER!".
I verified this by playing the game and confirming the hint matched the guess.

**Incorrect/misleading suggestion:**
Copilot initially suggested check_guess return just a string like "Win",
but the function actually returns a tuple like ("Win", "🎉 Correct!").
The tests were written to compare against just the string, so they failed.
I had to manually fix test_game_logic.py to use result[0] to access
the first element of the tuple.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?

---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.
