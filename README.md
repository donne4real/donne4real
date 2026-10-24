# Hey, I'm Leye 👋

**AI Engineer** — production speech-to-text, translation, and local-LLM systems.

I'm a BI Architect moving into AI engineering. I build systems that do real inference work,
and I measure them against gates defined *before* I start building.

🌐 **Portfolio:** https://leye-ajibola.netlify.app
📫 **Email:** leyeajibola@gmail.com
💼 **LinkedIn:** https://www.linkedin.com/in/donne4real

---

## 🔬 Flagship — Aso Oke

**Closing the AI gap for Yoruba.** OpenAI's Whisper large-v3 scores a **92.6% word-error rate**
on Yoruba — essentially unusable for tens of millions of speakers.

I measured the baseline first, then built against it: a custom diacritic normalizer, a
per-dataset licence-audited data pipeline, and a **pre-registered three-path ship gate**.

The honest outcome is the interesting one:

| Model | FLEURS Yoruba test WER | Note |
|---|---|---|
| Whisper large-v3, no fine-tune | 92.6% | the floor |
| Whisper large-v3 + LoRA, 8 epochs | 61.4% | **my own fine-tune — failed the gate** |
| Omnilingual ASR LLM 1B, as-is | **32.0%** | zero Yoruba training — **shipped** |

I chose the baseline over my own model, and documented exactly why. 4.12s p95 latency on a
single T4, a $400 hard compute ceiling, and a public decision log.

→ [`github.com/donne4real/aso-oke`](https://github.com/donne4real/aso-oke) · ships 13 Dec 2026

---

## 🚀 Live demos

| Project | What it is | Link |
|---|---|---|
| **Word Up** | Offline-first Bible reader, 22 translations, 45 tests | [bible-app.leyesapps.workers.dev](https://bible-app.leyesapps.workers.dev) |
| **NGX Tracker** | ~146 Nigerian Exchange stocks, tracked live | [ngx-tracker.pages.dev](https://ngx-tracker.pages.dev) |
| **Cert Mastery** | 300 questions each for AWS, Security+, CISSP, PMP, NCE, NCMHCE | [cert-mastery.netlify.app](https://cert-mastery.netlify.app) |
| **Powerball Predictor** | Hot/cold + due-number analysis over 296 draws, 4 weighted strategies | [powerball-predictor.netlify.app](https://powerball-predictor.netlify.app) |
| **Exam Prep NG** | WAEC / NECO / JAMB question banks, 12 subjects, CI/CD-validated | [donne4real.github.io/exam-prep-ng](https://donne4real.github.io/exam-prep-ng/) |
| **PocketOffice** | Writer, Calc, Impress, text editor and PDF tools in a browser | [donne4real.github.io/PocketOffice](https://donne4real.github.io/PocketOffice/) |
| **Tappers' Apprentice** | Interactive Nigerian-set story, custom JS engine | [donne4real.github.io/tappers-apprentice](https://donne4real.github.io/tappers-apprentice/) |
| **Daily Plan** | Scheduling and task views | [leyes-daily-plan.netlify.app](https://leyes-daily-plan.netlify.app) |
| **Vocabulary App** | Spaced-repetition vocabulary building | [build-my-vocab.netlify.app](https://build-my-vocab.netlify.app) |
| **Nia The Investigator** | Interactive investigation experience | [niatheinvestigator.netlify.app](https://niatheinvestigator.netlify.app) |

---

## 🧠 AI / ML work

| Project | What it is |
|---|---|
| [Aso Oke](https://github.com/donne4real/aso-oke) | Yoruba STT + translation, LoRA fine-tuning, pre-registered gates |
| [DataInsight](https://github.com/donne4real/datainsight) | Offline local-LLM data analyst — 100% on-device, no API key |
| [DocSummarization](https://github.com/donne4real/DocSummarization) | PDF and multi-file summarisation with a Streamlit UI |
| [Exam Prep NG](https://github.com/donne4real/exam-prep-ng) | Scripted curriculum pipeline generating question banks at scale |
| [MarketSage](https://github.com/donne4real/MarketSage-Analyzer) | Stock screener across 10 investment philosophies |

## 🛠 Engineering work

[Word Up](https://github.com/donne4real/bible-app) · [Cert Mastery](https://github.com/donne4real/cert-mastery) ·
[NGX Tracker](https://github.com/donne4real/ngx-tracker) · [PocketOffice](https://github.com/donne4real/PocketOffice) ·
[Powerball Predictor](https://github.com/donne4real/powerball-predictor) · [Vocabulary App](https://github.com/donne4real/vocabulary_app)

---

## 🧰 Toolkit

**AI/ML** — Python · PyTorch · PEFT/LoRA · Hugging Face · Transformers · Gradio · FastAPI · Flask · W&B
**Frontend** — React · TypeScript · Tailwind · Cloudflare Workers · JavaScript · PWA
**Data/Infra** — GitHub Actions · Cloudflare Pages · Netlify · R/Shiny · Databricks · SQL

---

## 🧭 How I work

- **Define the bar before you build.** Write the ship threshold down first, then let the result decide.
- **Licence before you baseline.** Half my architecture calls on Aso Oke came from licence audits — one of them would have permanently blocked monetising the product if I'd found it at launch instead of in Week 1.
- **Say what doesn't work.** The model cards state the gaps as plainly as the wins.
- **Ship the boring parts too.** CI/CD that validates data before every build; 45-test suites; accessible, responsive UIs.

---

## 📍 Currently

- 🔨 **Building** — Aso Oke, shipping 13 Dec 2026
- 📚 **Learning** — AWS AI & ML Scholars Nanodegree
- 🌍 **Based in** — Nigeria, working remotely

---

*Every number on this page is measured, not estimated. Source for all claims: the repositories above.*
