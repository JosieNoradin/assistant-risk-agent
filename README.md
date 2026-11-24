# 🌸 Assistant Risk Agent

**An AI risk engineer agent you can set up in minutes and adapt to your own projects.**

Assistant Risk Agent is a set of plain-text instruction files that turns an AI agent into a careful, friendly risk engineering colleague. It reviews risk registers, compares contractor risk reports month to month, and checks registers and reports against a Risk Management Plan.

It never changes your risk data without approval.

> Assistant Risk Agent supports the Risk Engineer. It does not replace the Risk Engineer.

---

## 💜 What it does

| Workflow | What Assistant Risk Agent does |
|---|---|
| **Risk register review** | Checks an Excel register for missing information and high-exposure risks, and proposes changes. It saves to a new file, never over your original. |
| **Contractor monthly report review** | Compares this month's report with last month's, flags unexplained changes and overdue actions, and drafts neutral clarification comments for you to approve. |
| **Risk compliance review** | Checks a Risk Register and Risk Report against the Risk Management Plan, recomputes every score, and produces an evidence-cited findings table. |

## ✨ How it's built

```
assistant-risk-agent/
├── AGENTS.md            ← the agent's role, rules and approval gates
├── User.example.md      ← template: who you are and how you like to work
└── workflows/
    ├── risk-register-review.md
    ├── contractor-monthly-risk-report-review.md
    └── risk-compliance-review.md
```

- **`AGENTS.md`** is the agent's job description: its role, operating principles, risk register rules, and what needs human approval.
- **`User.md`** tells the agent about you: your name, role, working style and reporting priorities.
- **`workflows/`** holds step-by-step procedures. `AGENTS.md` routes each task to the right one.

## 🚀 Getting started

1. Download or clone this repository.
2. Copy `User.example.md` to `User.md` and fill in the `[brackets]` with your own details.
3. Point your AI agent at the folder. Any agent that reads an `AGENTS.md` file will work, for example Claude, Hermes or another coding agent.
4. Ask it to do a task, such as *"Review this month's contractor risk report against last month's."*

## 🛡️ Design principles

- **Scripts do deterministic work, AI interprets evidence, and the Risk Engineer approves material decisions.**
- Never invent owners, dates, costs, probabilities or impacts.
- Every finding cites its source document, row and Risk ID.
- Risk scores are recomputed with tools, not with AI arithmetic.
- Source documents are treated as read-only.

## 🔧 Adapting it

- **Add a workflow:** create a new `.md` file in `workflows/` and add a routing line for it in `AGENTS.md`.
- **Change the tone:** edit the Communication Style sections.
- **Match your methodology:** update the risk review priorities in `User.md` to your organisation's criteria.

---

Made by [Josie](https://github.com/JosieNoradin), a Lead Risk Engineer who got tired of checking risk registers by hand. 🌷

Licensed under the [MIT License](LICENSE). Use it, adapt it, share it.
