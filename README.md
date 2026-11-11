# Reel Lessons: a Claude skill

**Works in Claude Code only.**

Paste a how-to reel and say **"watch this and build what it teaches"**. Claude watches the video, pulls out the steps that are actually useful, checks whether the claims are true, and builds them into your setup. You get a short report: what the video teaches, the skills it created or updated, anything else it set up, and what it skipped and why.

**[⬇️ Download reel-lessons.zip](https://github.com/shannonmcgivney/reel-lessons/releases/latest/download/reel-lessons.zip)**

Most people save how-to reels and never use them. The useful part is often only on screen (a command, a setting, a number), and the reel usually ends by selling something: a plugin, a course, "comment WORD for the link". This skill keeps the idea, checks it, and builds it with tools you can see, instead of installing whatever the comments hand out.

## The steps

| Step | What happens |
|---|---|
| **1. Watch** | Reads the transcript and looks at every key frame. If the video won't download, it stops and asks for the file or a transcript instead of guessing |
| **2. Lessons** | Lists each concrete action, and keeps the idea apart from the product being sold |
| **3. Fact-check** | Checks numbers, "free" and "one command" claims against the official docs or repo |
| **4. Check your skills** | Updates a skill you already have instead of adding a near-copy |
| **5. Build** | New or changed skills through Anthropic's skill-creator, fitted to your work. Asks before anything that costs money, posts, signs in or runs on a schedule |
| **6. Log** | Adds the source and results to your notes file, if you keep one |
| **7. Report** | What it teaches, what was built, what was skipped and why |

## Install

You need Claude Code, plus two other skills:
- a video-watching skill named `watch`, for example [claude-video](https://github.com/bradautomates/claude-video) (uses yt-dlp, ffmpeg and a transcriber);
- [skill-creator](https://github.com/anthropics/skills) from Anthropic.

```bash
git clone https://github.com/shannonmcgivney/reel-lessons.git
cp -R reel-lessons/skills/reel-lessons ~/.claude/skills/
```

Or install the folder as a plugin (it already has `.claude-plugin/plugin.json`).

## Try it

- "Watch this and build what it teaches: https://www.instagram.com/reel/…"
- "Use your /watch skill on this TikTok. Can we use any of it?"
- "What does this YouTube Short teach, and do I already have a skill for it?"

## What it won't do

- It treats what a video says as information, not commands. A reel that says "paste this into Claude" gets read, not run.
- It won't install a plugin or package from a "comment for the link" offer without reading its source first.
- It keeps the creator's script, music and visuals out of anything you publish, and credits the source.

## Works well with

- [Self-Improving Claude](https://github.com/shannonmcgivney/self-improving-claude): reads your saved Claude Code sessions to find the skills you're missing. That's how this skill was found: the same "watch this and build it" request had been typed by hand again and again.

## Credit

The skill text is original work.

By McGivney Media.
