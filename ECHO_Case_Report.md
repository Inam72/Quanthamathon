
# ECHO — Case Report

**Entangled Minds: The Quantathon · Qubits Qrew, NED University**  
**Investigator:** Inam (GitHub: Inam72) **Team:** Inam  
**Modules:** 01, 03, 05 (mandatory) · 02 (stretch)

## 1. Verdict

**ECHO never sent a message faster than light, and it didn't start by chance.**

*Physics.* Zara's detectors always agreed, and she took that as proof they were talking. Agreeing isn't sending. Each detector alone gives random results nobody can control, so no message can go in. You only see the agreement by comparing results afterwards over a normal channel, which is no faster than light.

*People.* The "random" coin that triggered ECHO was loaded to 70/30 (Module 02). My best guess: **Vance set it up**, so ECHO would fake a "success" he could later expose, and **Sana either helped or missed it**. I can prove the coin was loaded, not who loaded it.

**Confidence:** ~90% ECHO couldn't send anything. ~80% the coin was loaded on purpose. Low on who.

## 2. Evidence Board

Each row links something I measured or found to what someone claims, what I think it means, and what's still unanswered.

| FACT | CLAIM | INFERENCE | OPEN QUESTION |
|---|---|---|---|
| A real entangled pair and two people sharing a secret coin flip **both** only give `00`/`11` (Module 03 Silver) | **Zara:** "They told me entanglement could never carry a message. I proved them wrong." | "Always agreeing" can't tell a quantum link from a shared secret, so her proof doesn't show a message | — |
| Only the real pair keeps agreeing after an H, but each side on its own is still random (Module 03 Gold) | **Vance:** "ECHO was never real." | Vance is right about the physics: the link is real, but nothing can be sent through it | Did he know because he planted the flaw? |
| The trigger coin `ry(1.159)` lands on 0 about **70%** of the time, not 50% (Module 02) | **ARIA:** "No unauthorised command was issued." | ARIA just ran it. Someone *with permission* set the coin | Who configured ARIA's run, and when? |
| 1.159 is almost exactly the setting for a clean 70/30 coin (Module 02 Gold) | **Sana:** "I only deleted a corrupted log." | Accidents don't land on neat numbers. The coin setting would be in the logs, and the only person who could edit them deleted one | What was in that log? |
| Bilal's report is missing (case file) | **Bilal:** "I warned her. Nobody listened." | He probably spotted the loaded coin. Someone who rigged it wouldn't warn her | Who removed his report? |
| Her last message decodes to **ECHO** (Module 05) | **Zara's note:** "Find the flaw before *they* bury it with me." | She knew someone wanted the flaw hidden. "They" points to more than one person, which fits Vance and Sana together | Who is "they"? |

## 3. Key Experiments

| Module | Circuit | Result | What it shows |
|---|---|---|---|
| 03 Silver | `h`, **measure**, `cx` (secret coin) vs. `h`, `cx` (real pair) | both only `00`/`11` (495/529 vs. 522/502) | Agreeing proves nothing on its own |
| 03 Gold | same pairs, `h` on both before measuring | real pair still agrees (488/536); secret coin gives all four (~25% each) | The link is real, but each side alone is random |
| 02 Silver / Gold | `ry(1.159)`, measure | ~70/30, about 13 times past a fair coin's normal drift; ~56 flips is enough to catch it | The trigger coin was rigged |
| 05 Bronze | majority vote on the 96-bit stream | **ECHO** | Her last message, recovered |

All run on the Qiskit simulator.

## 4. What It Means

Zara's proof can't tell a real quantum link from a pre-agreed coin flip, and even a real link gives each side results it can't control. They agree, but nothing gets sent.

The coin is a different story. 1.159 is almost exactly the setting for a clean 70/30, which looks chosen, not accidental. ARIA only ran what it was given. Bilal warned her, which a rigger wouldn't do. That leaves Vance (motive, know-how) and Sana (access, deleted log). Vance alone would need access the case file never gives him, and the change would show in Sana's logs, so he most likely needed her help, or she didn't check.

## 5. Other Explanation

The strongest alternative is that this was **an honest mistake**: Bilal or Zara set the coin wrong without realising, and nobody tampered with anything.

I don't find this convincing. Real mistakes tend to be messy, but this setting lands almost exactly on a clean 70/30. On top of that, the two things that could have exposed it, Bilal's report and the deleted log, have both disappeared. Still, I can't rule it out completely, which is why I hold my verdict at about 80% rather than certain. Either way, a loaded coin can't make ECHO truly faster than light. It can only make it *look* like it worked.

## 6. Next Experiment

Get ARIA's settings history and the deleted log back, and check who set `ry(1.159)` and when, compared with the final run and Sana's deletion.

## 7. Limitation

I can prove the coin was loaded, not who loaded it. Everything ran on a simulator, not real hardware.

## 8. AI Acknowledgment

I used Claude (an AI assistant) to help me understand concepts, check my code, and organise this report.
