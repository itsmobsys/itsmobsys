<!-- ╔══════════════════════════════════════════════════════════════╗ -->

<!--                      GITHUB PROFILE                          -->

<!-- ╚══════════════════════════════════════════════════════════════╝ -->

<div align="center">

# ⚡ HEY, I'M DEV

### `@itsmobsys`

**I build things because I want to know how they work.**

<a href="https://github.com/itsmobsys">
  <img src="https://img.shields.io/badge/GitHub-itsmobsys-181717?style=for-the-badge&logo=github&logoColor=white" />
</a>
<a href="https://github.com/itsmobsys?tab=repositories">
  <img src="https://img.shields.io/badge/Projects-Browse-2ea44f?style=for-the-badge&logo=github&logoColor=white" />
</a>

<br><br>

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=2800&pause=900&center=true&vCenter=true&width=700&lines=Building+ClipWave;Python+%7C+JavaScript+%7C+Linux;Performance+%7C+Automation+%7C+Backend;Breaking+things+to+understand+them;Build+it.+Break+it.+Make+it+better." />

</div>

---

# 🧠 About Me

I'm a developer who enjoys building **real projects, solving weird problems, optimizing things that probably didn't need optimizing, and then finding out why everything broke.**

I like working on software where the interesting part isn't just the UI.

The stuff underneath matters too:

```text
┌───────────────────────────────────────────────────┐
│                    HOW I BUILD                    │
├───────────────────────────────────────────────────┤
│                                                   │
│   idea                                            │
│    ↓                                              │
│   prototype                                       │
│    ↓                                              │
│   break it                                        │
│    ↓                                              │
│   understand why                                  │
│    ↓                                              │
│   optimize                                        │
│    ↓                                              │
│   test it                                         │
│    ↓                                              │
│   ship it                                         │
│                                                   │
└───────────────────────────────────────────────────┘
```

I care about software that is:

> **Fast · Lightweight · Reliable · Maintainable · Actually useful**

---

# 🚀 What I'm Building

## 🎬 ClipWave

A streaming-focused platform built around clipping content from:

**YouTube · Twitch · Kick**

But I'm not only interested in the frontend.

I'm also building the infrastructure around it:

| System              | What I'm working with                      |
| ------------------- | ------------------------------------------ |
| 🎥 Stream discovery | Finding and tracking streams               |
| 💬 Live chat        | Processing and synchronizing live messages |
| 🎮 Game detection   | Identifying games from YouTube data        |
| ⚡ Caching           | Reducing unnecessary requests              |
| 🔌 APIs             | Connecting the systems together            |
| 🤖 Automation       | Making repetitive work disappear           |
| 🧠 AI / LLMs        | Experimenting with useful AI workflows     |
| 🖥️ Infrastructure  | Keeping things lightweight and reliable    |
| 📊 Performance      | Measuring instead of guessing              |

---

# ⚙️ My Engineering Philosophy

I like solving problems that look something like this:

```text
          BEFORE

     Request arrives
            │
            ▼
      Do expensive thing
            │
            ▼
      Do expensive thing
            │
            ▼
      Do expensive thing
            │
            ▼
        Return result


          AFTER

     Request arrives
            │
            ▼
       Check memory
            │
       ┌────┴────┐
       │         │
      HIT       MISS
       │         │
       ▼         ▼
    Return     Check DB
                 │
            ┌────┴────┐
            │         │
           HIT       MISS
            │         │
            ▼         ▼
         Return    One request
                       │
                       ▼
                    Cache it
                       │
                       ▼
                    Return
```

I don't particularly care about writing the **most** code.

I'd rather write:

```text
less code
   ↓
less complexity
   ↓
less work
   ↓
less resource usage
   ↓
fewer failure points
```

And when something does need to be complicated, I want to know **why**.

---

# 🎮 Featured Project

## Game Sorting for ClipWave

**YouTube video → game detection → cached result**

A lightweight Python module designed to identify the game associated with a YouTube video without throwing a giant stack of dependencies at the problem.

### ✨ The design

```text
                  YouTube Video
                        │
                        ▼
                 Validate ID
                        │
                        ▼
                 L1 Memory Cache
                    │       │
                  HIT       MISS
                    │       │
                    ▼       ▼
                 Return   L2 SQLite
                              │
                         ┌────┴────┐
                         │         │
                        HIT       MISS
                         │         │
                         ▼         ▼
                      Return   HTTP request
                                   │
                                   ▼
                              Extract game
                                   │
                                   ▼
                              Store result
                                   │
                                   ▼
                                Return
```

### 🔥 Things I specifically cared about

* No browser automation
* No LLM calls
* Minimal dependencies
* Two-level caching
* SQLite persistence
* Request coalescing
* Bounded concurrency
* TTL-based expiration
* Graceful failures
* Automated tests
* Resource measurements
* Predictable memory usage

### 🧪 The interesting part

When multiple callers ask for the **same video simultaneously**, they shouldn't all independently hit YouTube.

Instead:

```text
Caller 1 ─┐
Caller 2 ─┤
Caller 3 ─┼──► ONE HTTP REQUEST
Caller 4 ─┤
Caller 5 ─┘
                 │
                 ▼
             Shared result
```

That's the sort of optimization I enjoy finding.

<br>

<a href="https://github.com/itsmobsys/Game-sorting-for-clipwave">
<img src="https://img.shields.io/badge/VIEW_PROJECT-Game--sorting--for--ClipWave-000000?style=for-the-badge&logo=github&logoColor=white">
</a>

---

# 🛠️ Tech Stack

### Languages

<p>
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
<img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" />
<img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" />
</p>

### Backend & Data

<p>
<img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white" />
<img src="https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white" />
<img src="https://img.shields.io/badge/REST_APIs-FF6F00?style=for-the-badge&logo=fastapi&logoColor=white" />
</p>

### Tools & Platforms

<p>
<img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" />
<img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" />
<img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" />
<img src="https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white" />
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
</p>

### Currently Exploring

```text
AI / LLMs
Cloud Infrastructure
Backend Architecture
Performance Engineering
Automation
Distributed Systems
Linux Internals
Developer Tooling
```

---

# 📊 GitHub Overview

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=itsmobsys&show_icons=true&hide_border=true&theme=transparent&rank_icon=github" height="180"/>

<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=itsmobsys&layout=compact&hide_border=true&theme=transparent" height="180"/>

<br>

<img src="https://streak-stats.demolab.com?user=itsmobsys&hide_border=true&theme=transparent" height="180"/>

</div>

---

# 📈 Contribution Graph

<div align="center">

<img src="https://github-readme-activity-graph.vercel.app/graph?username=itsmobsys&bg_color=00000000&hide_border=true&area=true&custom_title=Vikram's%20Contribution%20Graph" width="95%"/>

</div>

---

# 🧩 Projects

| Project                          | Description                                 | Focus                          |
| -------------------------------- | ------------------------------------------- | ------------------------------ |
| 🎬 **ClipWave**                  | Streaming-focused clipping platform         | Web · Backend · Infrastructure |
| 🎮 **Game Sorting for ClipWave** | Lightweight YouTube game detection          | Python · SQLite · Caching      |
| 🌐 **boink_2068**                | Personal website / experimental web project | JavaScript · Web               |

More experiments, tools and projects will keep appearing here as I build them.

---

# 🧪 Things I Like Optimizing

### 🌐 Network

```text
Can I avoid the request?
        ↓
Can I cache the result?
        ↓
Can requests share the same work?
        ↓
Can concurrency be bounded?
        ↓
Can failure be graceful?
```

### 💾 Memory

```text
How much RAM does this actually use?

Not:
    "It should be fine."

But:
    measure it
    test it
    stress it
    find the limit
```

### ⚡ Performance

I like benchmarks because:

> **"It feels faster" isn't a measurement.**

---

# 🧠 What I'm Learning

I'm constantly working on becoming better at:

* Software architecture
* Backend engineering
* Linux internals
* Cloud infrastructure
* Performance optimization
* AI-assisted development
* Automation
* Building larger systems
* Maintaining projects over time
* Turning prototypes into reliable software

---

# 🔬 A Few Rules I Try To Follow

```text
┌──────────────────────────────────────────────┐
│  01  Measure before optimizing               │
│  02  Cache before repeating work             │
│  03  Fail gracefully                         │
│  04  Keep dependencies intentional            │
│  05  Prefer simple systems                   │
│  06  Test the weird cases                    │
│  07  Understand the bottleneck               │
│  08  Don't optimize imaginary problems       │
│  09  Automate repetitive work                │
│  10  Ship things people can actually use     │
└──────────────────────────────────────────────┘
```

---

# 🤖 AI & Development

I use AI as a **tool**, not as a replacement for understanding the software.

My preferred workflow is roughly:

```text
Human idea
    ↓
AI-assisted exploration
    ↓
Prototype
    ↓
Read the code
    ↓
Break the code
    ↓
Understand the code
    ↓
Fix the architecture
    ↓
Test
    ↓
Ship
```

The goal isn't to generate more code.

The goal is to **build better software faster**.

---

# 🧰 My Favorite Kind of Problem

Something nobody notices until you look closely.

For example:

```text
"Why are we making 10,000 requests?"

"Why does this use 500 MB?"

"Why are five workers doing the same thing?"

"Why does this work until two users arrive?"

"Why are we launching a browser for something
that could be solved with one HTTP request?"
```

Those are fun problems.

---

# 🌱 Still Building

I'm still early in the journey, which means there is a lot left to learn.

There will be:

```text
more projects
more bugs
more experiments
more optimizations
more terrible ideas
more surprisingly good ideas
```

And hopefully, a lot more things worth showing here.

---

# 📌 Explore

<div align="center">

<a href="https://github.com/itsmobsys?tab=repositories">
<img src="https://img.shields.io/badge/ALL_REPOSITORIES-181717?style=for-the-badge&logo=github&logoColor=white" />
</a>

<a href="https://github.com/itsmobsys/Game-sorting-for-clipwave">
<img src="https://img.shields.io/badge/FEATURED_PROJECT-2ea44f?style=for-the-badge&logo=github&logoColor=white" />
</a>

</div>

---

<div align="center">

### 💭 "Build it. Break it. Understand it. Make it better."

<br>

<sub>
Made with curiosity, questionable amounts of debugging, and probably too many optimizations.
</sub>

<br><br>

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=120&section=footer"/>

</div>
