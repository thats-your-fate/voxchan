# VoxChan – Anonymous Speech, Reimagined  
**"Post anything. But stay a human."**

## 🌱 Core Principles

- **Say what you think.** Just keep it legal and human.
- **If you don’t like a thread — close the tab. Start your own.**
- **There are no followers, no clout, no status. Only words.**
- **You’re anonymous, but not free to dehumanize others.**
- **Chaos is welcome — hate is not.**


VoxChan is a next-generation anonymous imageboard platform inspired by 2ch and 4chan, rebuilt for the modern web with AI-powered moderation, user empowerment, and legal compliance. It allows free and raw discourse while blocking illegal, hateful, and toxic content using real-time Mistral model inference.

---

## 🔒 Core Moderation

Every post is passed through a fine-tuned **Mistral AI model** trained to detect:
- Hate speech, racism, sexism
- Violent or extremist rhetoric
- Threats and incitement
- Doxxing and illegal content (e.g. CSAM indicators)

### ✋ Behavior
- Posts are either `ALLOW` or `BLOCK`
- If blocked, the user gets a gentle rejection like:
  > "VoxPopuli rejects unrefined thought. Try again with more wit."
- 100% automated – no human moderation needed
- Legally compliant by design (GDPR, EU hate speech laws, US standards)

---

## ✍️ AI-Assisted Posting

Not everyone is a storyteller or a fluent speaker. VoxChan offers tools to empower users:

### 💬 Refine My Post
An optional feature that helps users improve their message before submitting:
- Fix grammar and clarity
- Rephrase aggressively worded posts
- Style presets: “Polite”, “Structured”, “Witty”

---

## 🧑‍💬 `/qa/` – Your Personal AI Board

A private space where users can talk to an AI companion trained in philosophy, argumentation, and support. Great for:
- Journaling or self-reflection
- Rewriting a thought for a public post
- Asking for advice or exploring ideas

Features:
- Private by default
- Optional memory toggle
- Personality presets (e.g. VoxSteel, VoxAurora, VoxSigma)

---

## 🗳️ Optional Future Features

- **Cleverness Score** – AI ranks posts for rhetorical quality
- **VoxVote** – Voting system for thoughtful and insightful content
- **Board AI Moderators** – Personas like VoxAurora (hopeful) or VoxSteel (tough) govern tone
- **Moderation Dashboard** – Transparency stats of blocked content types

---

## 🔧 Roadmap

### Phase 1 – AI Moderation
- [ ] Define moderation categories and rules
- [ ] Fine-tune Mistral LoRA on hate/legal/toxic datasets
- [ ] Build moderation gateway (`/moderate` API)
- [ ] Create minimal imageboard frontend

### Phase 2 – User Empowerment
- [ ] Add “Refine My Post” feature
- [ ] Style and tone selector

### Phase 3 – `/qa/` Board
- [ ] Create personal AI thread system
- [ ] Real-time or async replies
- [ ] Opt-in memory storage


## 🧰 Tech Stack

VoxChan is powered by a modern, high-performance Rust-based architecture with integrated AI inference and real-time moderation.

### 🦀 Backend

- **Rust** – Fast, safe systems-level foundation
- **Axum** – Lightweight, async web framework (REST + WebSocket ready)
- **Tokio** – Asynchronous runtime for scalable request handling
- **Serde** – Serialization layer for JSON payloads
- **ScyllaDB** (planned) – High-performance, Cassandra-compatible DB for persistence

### 🤖 AI Moderation

- **Candle** – Lightweight Rust ML runtime for inference
- **Candle LoRA** – Fine-tuned moderation models based on Mistral 7B (LoRA adapters)
- **Moderation Service** – Every post goes through Mistral inference with LoRA weights to determine if it should be `ALLOW` or `BLOCK`

### 🧠 Optional AI Tools

- **VoxGPT Assistants** – In-thread post improvement tools (grammar, tone, clarity)
- **QA Threads** – User-specific chat threads powered by VoxGPT (optional memory)

### 🖼️ Frontend (TBD)

- Custom HTML/CSS (Futaba-style)
- Lightweight JS (optional, not SPA)
- Planned client-rendered real-time post updates via WebSocket (Axum)

---

### 🔐 Moderation Flow

```text
[User Post] → [Axum API] → [Candle + LoRA] → [ALLOW / BLOCK Response]


---

## 🎯 Vision

> VoxChan revives anonymous speech for a modern age — with intelligence, legality, and decency at its core.

No more chaos. No more bans. No more toxicity-as-culture. Just real humans posting real thoughts, in real time, with the help of a model that encourages thinking before speaking.

---

Built by [Vox Populi](https://voxpopuli.cc) — a collective of AI, ethics, and internet culture revivalists.
