# Lisa

Lisa is a personal learning assistant you work with inside Claude Desktop. You
name something you want to learn, and Lisa builds a course on it. Then she teaches
you one session at a time, quizzes you, and brings back what you missed until you
have it.

Your courses and your record of what you know stay on your own computer, in a
folder of plain files that you own.

**Status:** an early release (v0.1), tested on Windows. Feedback is very welcome
(see below).

## What she does

- **Builds a course from a topic.** Name any topic, or ask for some ideas. Lisa
  lays out units and lessons in teaching order. Topics in Personal Finance,
  Artificial Intelligence and Mathematics are placed on her own topic list,
  organized with an eye toward published standards. Any other topic works too.
- **Teaches, then checks.** Each lesson ends with a short quiz. Lisa's server
  scores every answer, not the chat, and records it as evidence.
- **Reviews on a schedule.** A miss comes back the next day. A topic you know
  comes back after longer and longer gaps as your level rises from basic to
  working, solid and mastered.
- **Shows where you stand.** Progress, quiz results and session summaries appear
  as cards in the chat.

## Standards

Lisa's topic lists are her own, organized with an eye toward published standards:
the National Standards for Personal Financial Education (2021), the Common Core
State Standards for Mathematics, and AI4K12's Five Big Ideas in AI. Lisa is not
affiliated with or endorsed by their publishers (the Council for Economic
Education and Jump$tart; the NGA Center and CCSSO; the AI4K12 Initiative).

## What you need

- Windows with [Claude Desktop](https://claude.ai/download), signed in.
- A Claude plan. Lisa is tested on Claude Pro. The Free plan is untested, and its
  usage limits may cut a session short.
- Python 3.11 or later, from [python.org](https://www.python.org/downloads/) or
  the Microsoft Store.

## Install

1. Download `lisa-<version>.zip` from the
   [latest release](https://github.com/bindrel-bfuller/lisa/releases/latest).
2. Right-click the zip, choose **Extract All**, and extract it to your user
   folder, `C:\Users\<you>`. This makes a folder named `Lisa-app`. Claude Desktop
   runs Lisa from that folder, so don't move or delete it. Avoid folders that
   OneDrive syncs, such as Documents or Desktop: OneDrive can make the files
   online-only.
3. Open the `Lisa-app` folder and right-click an empty space in it.
   - On Windows 11, choose **Open in Terminal**.
   - On Windows 10, hold Shift as you right-click and choose **Open PowerShell
     window here**.

   Then run:

   ```
   py setup.py
   ```

   If `py` is not found, run `python setup.py` instead. Don't double-click
   `setup.py`: its window closes before you can read what it says.
4. Quit Claude Desktop fully: close its window, then right-click Claude's icon in
   the system tray, near the clock, and choose **Exit**. Then open it again.
5. In a new chat, open the **+** menu and pick Lisa's **Set up** prompt.

To upgrade, extract the new release over the same folder and run `py setup.py`
again. Your courses and record are kept.

## Working with Lisa

Lisa's prompts are in the **+** menu of a new chat:

- **Set up**: your name and time zone, once.
- **Create a course**: name a topic, or leave it blank to get some ideas.
- **Start a session**: your next lesson, or a review if one is due.
- **Check progress**: where you stand in a course.
- **Help** and **Send feedback**.

After the first prompt, plain words work too: "keep going", "how am I doing?",
"that question is bad".

## Privacy

- **Your record stays on your computer.** Lisa keeps your courses, lessons,
  questions and record of answers in `%USERPROFILE%\Lisa`, as plain JSON and
  Markdown files. Lisa sends nothing over the network.
- **No account, no tracking.** Lisa has no sign-up of her own and collects no
  usage data.
- **The chat goes to Claude.** As in any Claude conversation, what you and Lisa
  say in the chat, including the lessons, your answers and what she shows
  from your record, goes to Anthropic under your Claude account's terms and
  privacy settings.
- **You can erase it.** Delete the `%USERPROFILE%\Lisa` folder to remove your
  courses and record. Lisa keeps no other copy; your past chats stay in Claude.
- **Feedback is public.** Posts in Discussions can be read by anyone, so leave
  out anything personal.

## Feedback

Start with the pinned [Feedback thread](https://github.com/bindrel-bfuller/lisa/discussions/5).
Bugs, confusing moments, bad questions and ideas are all useful. Pick **Send
feedback** from the + menu, and Lisa helps you write it up.

No GitHub account? Send it as a message to
[What's Known on LinkedIn](https://www.linkedin.com/company/whatsknown).

## License

Lisa is free for personal use and other noncommercial purposes under the
[PolyForm Noncommercial License 1.0.0](LICENSE). Using Lisa in a business,
including a company trial, needs written permission: ask through LinkedIn
(above).
