# Prompting Frameworks

Four Claude/Cowork skills for structuring and QA'ing prompts, built around GRC and audit-facing
work but generally applicable. Each `.skill` file is a ready-to-install package (zip a folder
containing `SKILL.md` — the standard Claude Code / Cowork skill format); import it directly, or
read the `SKILL.md` inside for the technique on its own.

See `AI_Prompting_Frameworks_Reference_Guide.docx` for the full writeup tying all four together.

## The four skills

| Skill | Use it for |
|---|---|
| `art-framework-prompting.skill` | Refining a vague, underspecified one-line ask before acting on it — a personal convention, not an industry-standard framework |
| `icio-framework-prompting.skill` | Structuring production LLM/API prompts (Instruction / Context / Input data / Output format) for pipelines where parseable output matters — n8n steps, scoring calls, structured DB writes |
| `cot-framework-prompting.skill` | Chain-of-Thought reasoning for multi-factor judgment calls (risk tiering, control effectiveness ratings, severity classification) before committing to a verdict — this one **is** a real, citable industry-standard technique, safe to reference by name in client-facing material |
| `reflexion-self-critique.skill` | A single-pass draft → critique-against-rubric → revise loop for any deliverable before finalizing it — audit findings, client memos, training content |

**ART vs ICIO vs CoT vs Reflexion, in one line each:**
- ART = sharpening what you ask Claude, conversationally
- ICIO = structuring a prompt that runs unattended against an API/parser
- CoT = forcing explicit reasoning before a judgment call
- Reflexion = QA'ing a finished draft against an explicit rubric before shipping it

ART and ICIO are personal conventions (not external frameworks — don't cite them as industry
standard in client-facing material). CoT is a real, citable technique. Reflexion is a
lightweight, single-model variant of self-critique prompting.

## Install

Each `.skill` file can be imported directly into Claude Code or Cowork's skill system. Or copy
the SKILL.md content into your own skill/plugin structure.
