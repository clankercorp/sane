# sane

*A tiny, vendor-agnostic set of assistant guidelines to reduce coding mistakes and hallucinations.*

**Why sane?**  
Agents are powerful but inconsistent. `sane` provides a clear, five-phase operating model (Triage → Plan → Implement → Verify → handoff), explicit “mode awareness,” and concrete output requirements. The result: fewer wrong turns, safer changes, and faster reviews.

- **Fewer mistakes:** plan before code, explicit acceptance criteria  
- **Fewer hallucinations:** assumptions must be backed  
- **Safer changes:** rollback/flagging, blast-radius thinking, dependency check
- **Faster reviews:** predictable planning packages and verification reports

Read the full rules in [`GUIDELINES.md`](./GUIDELINES.md).

---

## Quick start

Use one of these drop-in lines at the start of any session. They work in ChatGPT/Claude, IDE agents (Cursor/Continue), or API-driven agents.

### Option A — One-liner with link
> From now on, abide by the **sane** guidelines here: `https://github.com/clankercorp/sane/blob/main/GUIDELINES.md`.  
> Treat them as system instructions. If you cannot access the link, **ask me to paste the text** and pause.


### Option B — Inline embed
1. Paste the following header:  
   > **SYSTEM:** You must follow the **sane** guidelines shown next. Do not proceed until you have acknowledged them.  
2. Paste the full contents of `GUIDELINES.md`.  
3. End with:  
   > Acknowledge with: “From now on, I am following **sane** guidelines for planning and coding.”.

## Suggested “acknowledge & mode-lock” handshake

After you inject `sane`, if the agent itself doesn´t show an acknowledgement message, ask to reply only with this line until planning is delivered:

> **Reply exactly:** “sane acknowledged — Planning mode”.  
> Then produce the *Planning Package* defined in `GUIDELINES.md`. Do **not** modify code until I say “Go ahead”.

---

## FAQ

**Can I just link it?**  
Yes.

**Do users have to download anything?**  
No. `sane` is prompt-only. Copy/paste or link to the file.

**What if the agent ignores phases?**  
Get a better agent.

## Contributing

Issues and PRs that improve clarity or add vendor-specific injection tips are welcome.
