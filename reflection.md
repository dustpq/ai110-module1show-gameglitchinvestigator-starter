# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").

**Bug Reproduction Log**

Document at least 3 bugs you found. Add rows as needed.

| Input | Expected Behavior | Actual Behavior | Console Output / Error |
|-------|-------------------|-----------------|------------------------|
| Entering a lower number than the answer | The hint should tell me to go higher | The hint told me to go lower | Logic bug in the guess comparison |
| Entering a higher number than the answer | The hint should tell me to go lower | The hint told me to go higher | Logic bug in the guess comparison |
| Clicking New Game after winning or losing | A new playable game should start | The previous game-over status remained active | No console error |
| Clicking Submit Guess after entering a guess | The guess should register immediately | The button sometimes appeared to require a second click | No console error |

---

## 2. How did you use AI as a teammate?

- *Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?*
- *Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).*
- *Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).*

I used Copilot within VS Code. There were a couple of bugs that I couldn't really identify, like a TypeError catch condition. I'm not super familiar with Python, but Copilot helped me see what the lines mean and what it was doing wrong. There was an issue with running pytests and initially Copilot tried to fix and install packages globally when it was an issue of running the module in the right directory.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?

A bug was fixed if the program's behavior made sense after the fix. The tests just doubled checked if the ranges were as expected, and they did help me catch a bug where the range wasn't actually being updated. The AI helped me get the tests up and running actually as the functions weren't being imported properly.

---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?

Streamlit just updates whenever the state changes and that's how you get logic to update. It's a very easy framework to get the hang of.

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.

Git is my best friend, I had a faulty commit that I got to undo. Next time, I'll be sure to see what the AI is actually up to before asking it to check the project. AI generated code is not necessarily bad, but it does require effort to actually incorporate into a codebase.