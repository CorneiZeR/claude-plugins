<h1 align="center">claude-plugins</h1>

<p align="center"><em>Two skills, installable rather than copied.</em></p>

---

## Add it once

```
/plugin marketplace add CorneiZeR/claude-plugins
```

Then install whichever you want:

```
/plugin install nuclock@corneizer
/plugin install coderabbit@corneizer
```

`/plugin update` keeps them current, and `/plugin uninstall` takes one back
out. Nothing here is copied into your settings by hand, which is the whole
reason this repository exists: a skill that takes a clone, a symlink and an
edited `settings.json` is a skill most people never finish installing.

## What is in here

| Plugin | What it is for |
| --- | --- |
| [`nuclock`](https://github.com/CorneiZeR/nuclock-skill) | Working in the nuclock tracker: planning a backlog into a queue, seeing what is next and what is BLOCKED, taking one task from start to done, and keeping the timer honest. |
| [`coderabbit`](https://github.com/CorneiZeR/coderabbit-skill) | Reviewing with CodeRabbit: which surface to spend, how the hourly allowances behave, how to prove a head was really reviewed, and why a finding is a sample of a class rather than one site. |

This repository holds **only the list**. Each plugin lives in its own
repository, is versioned there, and is fetched from there — so a fix to a
skill does not need a change here, and adding a third skill does not touch
either of the first two.

## What a plugin may bring with it

Worth knowing before installing anything, here or elsewhere: a plugin can
carry **hooks**, and hooks run around tool calls in every session — not only
when you reach for the skill.

`nuclock` brings three, and all of them only print: the queue when a session
opens, a warning on the first edit if no timer is running, and a reminder at
the end if a timer was left running. None of them blocks an edit and none
writes time, for the same reason: a timer somebody did not start is time
nobody can vouch for. Its README says so in full, and it is the kind of thing
worth reading before a plugin is added to a machine.
