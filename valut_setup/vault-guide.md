# Knowledge Vault Setup Guide

*Optional. You don't need any of this to run the curriculum. This is for people who want a durable, searchable archive of their learning that survives platform changes, model updates, and the general impermanence of AI systems.*

---

## Why a Vault?

AI conversations are ephemeral by default. The platform might change, the model might update, your chat history might become inaccessible. If you're building a multi-month learning curriculum, that's a lot of thinking to lose.

The vault solves this. It's a local knowledge management system that holds your crystallizations, synthesis documents, syllabi, character files, and whatever else you want to preserve — all in plain Markdown files on your own machine. Nothing is locked into a proprietary format. Nothing depends on a specific app continuing to exist. If Obsidian disappeared tomorrow, you'd still have a folder of text files that any editor can open.

The vault also becomes a collaboration tool. When working with AI assistants (including Claude Code for vault maintenance), a well-structured vault with a specification file (CLAUDE.md) gives any AI immediate context about what you've built and how it's organized.

---

## The Stack

### Core

| Tool | Role | Cost |
|------|------|------|
| **Obsidian** | Local-first knowledge management app. All files are plain Markdown stored on your machine | Free |
| **Claude Pro** | AI platform for running the curriculum. Pro plan gives you Projects (persistent instructions and reference files) and longer conversations | $20/month |
| **iCloud Drive** (or your preferred cloud sync) | Syncs the vault between devices. Put the vault folder inside your iCloud Drive directory and it's available on your Mac, iPhone, and iPad | Included with Apple ecosystem |

### Obsidian Plugins

These are community plugins installed through Obsidian's settings. None are required, but they make the vault significantly more useful.

| Plugin | What It Does | Why It Matters |
|--------|-------------|----------------|
| **Dataview** | Treats your vault like a database. Query your files by tags, metadata, completion status | Lets you build dynamic indexes — e.g., "show me all episodes tagged with a specific character" or "list all open questions across crystallizations" |
| **Templater** | Advanced templates with dynamic content (dates, prompts, auto-filled fields) | Speeds up creating new episode notes, crystallizations, and synthesis documents with consistent structure |
| **Calendar** | Visual calendar view linked to daily notes | Useful for tracking when episodes were completed and seeing the curriculum timeline |

### Optional: Claude Code

For vault maintenance, auditing, and bulk operations (renaming files, checking link health, generating reports), Claude Code can work directly with your vault from the command line. This is how the vault audit referenced in this project was conducted — a read-only traversal that inventoried every file, checked wiki links, and identified gaps.

This is entirely optional and more advanced. You don't need it to build or maintain a vault.

---

## Vault Architecture

The vault uses a numbered-prefix system for top-level folders. This keeps them in a logical order in any file browser or app, regardless of alphabetical sorting.

### Recommended Structure for a Curriculum Vault

```
Your-Vault-Name/
├── 00-System/
│   ├── Memory-Snapshots/        ← Periodic exports of your AI memory/context
│   ├── Model-Context-Files/     ← Portable context files for AI handoffs
│   └── Raw-Exports/             ← Unprocessed conversation exports (if needed)
│
├── 10-[Your First Track]/       ← e.g., "10-Philosophy"
│   ├── _Index.md                ← Track overview, episode checklist, status
│   ├── Syllabus.md              ← Full curriculum plan
│   ├── Personas/                ← Character voice files
│   ├── Arc-1-[Name]/            ← Episode exports + crystallizations per arc
│   ├── Arc-2-[Name]/
│   ├── Arc-3-[Name]/
│   └── Synthesis/               ← Cross-arc synthesis documents
│
├── 20-[Your Second Track]/      ← Same structure, different subject
│   ├── _Index.md
│   ├── Syllabus.md
│   ├── Personas/
│   └── ...
│
├── 40-Integration-Hub/          ← Cross-track connections
│   ├── _Index.md
│   ├── Patterns/                ← Named patterns index, cross-domain map
│   └── Synthesis-Sessions/      ← Documents connecting insights across tracks
│
├── Templates/                   ← Reusable templates for episodes, checkpoints, etc.
│   ├── Episode-Template.md
│   ├── Checkpoint-Template.md
│   ├── Handoff-Template.md
│   └── General-Context-File.md
│
├── CLAUDE.md                    ← Vault specification for AI collaboration
└── README.md                    ← (Optional) Personal orientation to the vault
```

### How the Numbering Works

- **00** — System and infrastructure (not learning content)
- **10, 20, 30** — Individual learning tracks (Philosophy, Buddhism, Art, etc.)
- **40** — Integration hub (connections across tracks)
- **50+** — Other projects, personal content, etc.

The gaps between numbers are intentional — they leave room to add new tracks without renumbering everything.

### Key Files

**_Index.md** (one per track): The track's home page. Contains the episode checklist with completion status, links to key documents, and an overview of where the track stands. Think of it as the table of contents for that learning track.

**Syllabus.md** (one per track): The full curriculum plan — arc structure, episode topics, character assignments, key questions. This is the document you build collaboratively with the AI at the start of a track.

**CLAUDE.md** (root level): The vault specification. This file tells any AI assistant what the vault is, how it's organized, what's complete, what's in progress, and what conventions to follow. If you ever switch AI models, migrate platforms, or bring in Claude Code for maintenance, this file is the starting point. It's the single most important infrastructure file in the vault.

---

## Workflow: How the Vault Connects to the Curriculum

Here's how the pieces fit together in practice:

### During the Curriculum

1. **Claude Project** holds your active curriculum — project instructions, character guides, current crystallization
2. You run episodes in 5-episode chats inside the Project
3. After each 5-episode block, you crystallize and generate a handoff prompt
4. The crystallization document gets saved to the vault (in the appropriate arc folder)
5. The handoff prompt starts the next chat

### After Each Arc

1. Review the arc's crystallizations
2. Write (or collaboratively generate) an arc synthesis document
3. Save it to the vault's Synthesis folder for that track
4. Update the _Index.md with completion status

### After the Curriculum Completes

1. Export any raw conversation transcripts you want to preserve (save to arc folders or Raw-Exports)
2. Write a track-level synthesis document
3. If you have multiple tracks, create cross-domain documents in the Integration Hub
4. Update CLAUDE.md to reflect what's been completed

---

## Setting Up Your Vault

### Step 1: Install Obsidian

1. Download from [obsidian.md](https://obsidian.md) (free, Mac/Windows/Linux/iOS/Android)
2. Create a new vault. If you want cross-device sync, create it inside your iCloud Drive (Mac) or another cloud sync folder
   - On Mac: `~/Library/Mobile Documents/com~apple~CloudDocs/Your-Vault-Name/`
   - Or simply create it in your iCloud Drive folder visible in Finder
3. Open the vault in Obsidian

### Step 2: Install Plugins

1. Go to **Settings** → **Community plugins** → **Turn on community plugins**
2. Click **Browse** and search for each:
   - **Dataview** — install and enable
   - **Templater** — install and enable
   - **Calendar** — install and enable
3. For Templater: go to its settings and set your Templates folder to `Templates/`

### Step 3: Create the Folder Structure

In Obsidian's file browser (left sidebar):
1. Create your top-level folders using the numbered-prefix convention
2. Create subfolders per the structure above
3. Don't worry about populating everything immediately — create folders as you need them

### Step 4: Create CLAUDE.md

This is your vault specification. At minimum, it should contain:

```markdown
# [Your Vault Name] — Vault Specification

## Purpose
[What this vault is for — one or two sentences]

## Structure
[Brief description of the numbered-prefix system and what each top-level folder contains]

## Learning Tracks
### [Track Name] — [Status: Active / Complete / Planned]
- Episodes: [X/Y complete]
- Arcs: [list]
- Key files: [links to _Index.md, Syllabus.md]

## Conventions
- File naming: [your convention — e.g., "Arc-1-Foundations", "crystallization-ep1-5"]
- Wiki links: [[use these]] for internal cross-references
- Tags: [your tagging convention, if any]
- Templates: stored in Templates/ folder

## For AI Assistants
[Instructions for any AI working with this vault — what to read first, what conventions to follow, what not to modify without asking]
```

### Step 5: Add Templates

Create the templates in your `Templates/` folder. At minimum:
- An episode template (frontmatter + structure for episode notes)
- A crystallization template (the synthesis structure from the curriculum method)
- A handoff template (structure for generating the next chat's opening prompt)

These can be adapted from the templates in this GitHub repo.

---

## Syncing Across Devices

### iCloud (Apple ecosystem)

If your vault folder is inside iCloud Drive, Obsidian on your iPhone/iPad can open it directly. This gives you read access to your entire vault from your phone — useful for reviewing crystallizations, checking the syllabus, or reading synthesis documents on the go.

**Setup on iOS:**
1. Install Obsidian from the App Store
2. Open Obsidian → Create new vault → **Store in iCloud**
3. It should detect your existing vault folder

**Note:** Editing on iOS works but is slower than on a Mac. I'd recommend doing most writing and editing on your computer and using the phone primarily for reading and light edits.

### Other Sync Options

- **Obsidian Sync** ($4/month from Obsidian) — purpose-built, handles conflicts well
- **Dropbox, Google Drive, OneDrive** — all work the same way as iCloud (put the vault folder in the sync directory)
- **Git** — more advanced, but gives you version history. Better suited for people comfortable with the command line

---

## Scaling: Multiple Tracks

The vault architecture is designed to grow. When you start a second learning track:

1. Create a new numbered folder (e.g., `20-Whitman/`)
2. Add the same internal structure (_Index.md, Syllabus.md, Personas/, arc folders, Synthesis/)
3. Set up a separate Claude Project for the new track
4. As connections between tracks emerge, document them in `40-Integration-Hub/`

The Integration Hub becomes valuable once you have two or more tracks and start noticing patterns that cross domains. Named patterns that appear in both your philosophy and literature curricula, frameworks that transfer, questions that one track answered and another reopened — this is where that synthesis lives.

---

## A Realistic Note

This vault setup is the most comprehensive version. You don't need all of it to benefit from preserving your learning. A simpler version — just saving your crystallization documents in a folder on your computer — gets you 80% of the value. The Obsidian plugins, the numbered architecture, the CLAUDE.md specification, the cross-device sync — these are refinements for people who want to build a long-term knowledge system.

Start simple. Add structure as you need it. The vault should serve the learning, not the other way around.
