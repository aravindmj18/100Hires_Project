# Cursor IDE Setup with Claude and Codex

> Documenting the setup of Cursor IDE with Claude Code and Codex, including issues and solutions.
> 
## Table of Contents

- [Phase 1 — Environment Setup](#phase-1--environment-setup)
- [Phase 2 — Research Project](#phase-2---research-project)

# Phase 1 — Environment Setup

## Overview

This project focuses on completing the setup successfully while solving issues encountered during the process.


## Tools Used

- [Cursor IDE](https://cursor.com/) — AI-native code editor
- Claude Code Extension — AI coding assistant inside Cursor
- Codex Extension — Alternative AI coding extension
- Git + GitHub — Version control and remote repository


## Setup Walkthrough

### 1. Installing Cursor IDE
![Cursor Setup](assets/Image1.png)

Downloaded the installer from [cursor.com](https://cursor.com/) and followed the standard installation steps. No issues here — Cursor launched cleanly on the first try.

### 2. Creating a GitHub Repository

Created a new public repository on GitHub with a name and description, without initializing it with a README file.

### 3. Connecting the Repo to Cursor

Opened the repository inside Cursor and attempted to clone it locally. The initial attempt failed due to a missing dependency (Git). After resolving the issue, the repository was successfully cloned and connected.


### 4. Setting Up Claude Code

Searched for the Claude Code extension inside Cursor's extensions panel and installed it. Hit a wall immediately: logging in required a **Pro subscription**, which I didn't have at the time.

Rather than treating this as a blocker, I documented the limitation and moved on. Claude Code is on the list to explore once I have access.

### 5. Setting Up Codex

Installed the Codex extension through the same extensions panel, logged in without issues, and had it up and running as the primary AI assistant for this setup.


---

## Issues and How I Fixed Them

### 1. Git wasn't installed

![Cursor Setup](assets/Image2.png)

**What happened:**  
When I tried to clone the repository using Cursor IDE, the "clone repo" button did not respond. There was no error message or feedback, which made it unclear what the issue was.

**Why it happened:**  
Cursor relies on Git installed on the local system to perform repository operations. Since Git was not installed, the action could not be executed.

**How I identified it:**  
After checking basic setup steps and searching for similar issues, I found that Git is a required dependency for cloning repositories.

**What I did:**  
- Installed Git from [git-scm.com](https://git-scm.com/)  
- Verified the installation using `git --version` in the terminal  
- Retried the clone operation in Cursor  

**Outcome:**  
The repository was successfully cloned, and the issue was resolved.

### 2. Claude Code login restriction
![Cursor Setup](assets/Image3.png)

**What happened:** After installing the extension, I couldn't log in — it required a paid subscription.

**Why it happened:** This is just how the tool is priced. Not a bug, not a misconfiguration.

**What I did:** Noted it, switched to Codex for the rest of the setup, and kept moving. Sometimes the right move is just to work around a limitation rather than get stuck on it.

## Outcome

- Cursor IDE was successfully installed and configured  
- GitHub repository was created and connected  
- Repository was cloned successfully after resolving the Git issue  
- Codex extension was installed and used as the primary AI tool  
- Claude Code extension could not be fully used due to subscription requirement

### 6. Creating and Adding README.md

Created the README.md file manually inside Cursor IDE.

**How I did it:**  
- Opened the Explorer panel in Cursor (left sidebar)  
- Right-clicked on the project root folder and selected **New File**  
- Named the file `README.md` and created it  
- Added the documentation using Markdown syntax  

---

### 7. Pushing README.md to GitHub

After creating the file locally, I pushed it to the GitHub repository.

**Steps I followed:**
- Opened the integrated terminal in Cursor  
- Ran the following commands:

```bash
git add README.md
git commit -m "Add README.md"
git push -u origin main
```

## What I Took Away From This

This setup wasn’t very complex technically, but it made me realize how important the basics are.

- Most issues happened because something small was missing (like Git), not because the tool was broken  
- It’s better to understand why something failed instead of just trying random fixes  
- Writing things down while working helped me stay clear and actually understand each step  


---

# Phase 2 - Research Project

## Objective

To build a structured research repository analyzing how top B2B SaaS
practitioners design and execute cold outreach pipelines — with the
goal of extracting repeatable frameworks and developing a real-world
outbound playbook.

This is not a content aggregation project.  
The goal is **synthesis** — turning practitioner knowledge into
an actionable system.

---

## Topic Selected
**Cold Outreach Pipeline for B2B SaaS**

### Why This Topic
Cold outreach remains a high-ROI acquisition channel for
early-stage B2B SaaS — especially when paid ads are too expensive
and SEO is too slow to generate pipeline.

Most resources on this topic are either too generic or too
theoretical. This research focuses exclusively on **practitioners**
— people actively running outbound campaigns — to extract what
actually works in real-world outbound execution.

---

## Expert Roster

| # | Expert | Role | Primary Signal |
|---|--------|------|----------------|
| 1 | [Jason Bay](https://www.linkedin.com/in/jasonbay/) | Founder, Outbound Squad | Prospecting Systems + Outbound Messaging |
| 2 | [Nick Abraham](https://www.linkedin.com/in/nick-abraham/) | Co-founder, Leadbird | Cold Email Execution + Lead Generation |
| 3 | [Taylor Haren](https://www.linkedin.com/in/taylor-haren/) | Founder, Haren Media | Offer Positioning + Outreach Messaging |
| 4 | [Florin Tatulea](https://www.linkedin.com/in/florin-tatulea/) | B2B Growth Leader | Outbound Process + Pipeline Frameworks |
| 5 | [Steli Efti](https://www.linkedin.com/in/steliefti/) | CEO, Close | Outbound Psychology + Conversion Principles |
| 6 | [Armand Farrokh](https://www.linkedin.com/in/armand-farrokh/) | Sales Leader | Cold Calling + Outbound Execution |
| 7 | [Will Aitken](https://www.linkedin.com/in/willaitken/) | Sales Creator | Sales Conversations + Cold Calling Execution |
| 8 | [Yurii Veremchuk](https://www.linkedin.com/in/yurii-veremchuk/) | Cold Email Expert | Email Deliverability + Campaign Infrastructure |
| 9 | [Morgan J Ingram](https://www.linkedin.com/in/morganjingram/) | Founder, AMP Creative | Multi-Channel Outreach + Video Prospecting |
| 10 | [Josh Braun](https://www.linkedin.com/in/josh-braun/) | Founder, Braun Training | Messaging Psychology + Objection Handling |

### Why These Experts

These 10 were selected — not from the first page of Google —  
but based on four strict criteria:

- **Active execution** — they run real outbound campaigns  
- **Proven track record** — results in B2B SaaS environments  
- **Actionable content** — frameworks, scripts, real insights  
- **Pipeline coverage** — together they cover the full outbound system  

---

## Data Collected

For each expert:

- 🎥 2 YouTube videos → transcripts extracted using Supadata API  
- 💼 3–5 LinkedIn posts → manually curated high-signal content  

Current progress:

- ✅ Experts identified and documented  
- ✅ YouTube transcripts collected and organized  
- ✅ LinkedIn posts collected and structured  
- ✅ Framework extracted

All content is organized per expert and per source:

- `/Research/linkedin-posts/`
- `/Research/youtube-transcripts/`

This structure enables systematic analysis and playbook development.

---

## Tools & Workflow

- Used **Supadata API** to extract YouTube transcripts  
- Used **AI tools (Claude/Codex)** to:
  - Extract key takeaways  
  - Identify repeatable frameworks  

This workflow enables efficient data collection and structured synthesis.

---

## Pipeline Coverage Map

Every stage of a cold outreach pipeline is covered by at least
one expert in this research set:

- Targeting & Prospecting → Jason Bay, Nick Abraham  
- Messaging & Positioning → Taylor Haren, Josh Braun  
- Cold Calling & Conversations → Armand Farrokh, Will Aitken  
- Email Systems & Deliverability → Yurii Veremchuk  
- Multi-Channel Outreach → Morgan J Ingram  
- Full Pipeline Strategy → Florin Tatulea, Steli Efti  

---

## Next Steps

- Extract repeatable frameworks from each expert’s content  
- Identify cross-expert patterns in:
  - Messaging  
  - Prospecting  
  - Outreach execution  
- Synthesize findings into a structured cold outreach playbook  
- Translate insights into a step-by-step outbound pipeline system  

---

## Key Focus

This project prioritizes:

- Quality over quantity  
- Practical frameworks over generic advice  
- Real-world execution over theory  

The end goal is to build a **usable outbound system** — not just a collection of notes.

---


## Author

**Aravind Mudraveni**  
Aspiring AI Growth Marketer | Digital Marketing & Tech Enthusiast
