# Hey, I'm Leye 👋

**AI Engineer** — production speech-to-text, translation, and local-LLM systems.

I'm a BI Architect moving into AI engineering. I build systems that do real inference work,
and I measure them against gates defined *before* I start building.

🌐 **Portfolio:** https://leye-ajibola.netlify.app
📫 **Email:** leyeajibola@gmail.com
💼 **LinkedIn:** https://www.linkedin.com/in/donne4real

---

## 🧑‍🏫 New to AI? Start here

This page is written for engineers, so here's the two-minute version in plain terms.

**What I actually do.** I make software that understands speech and language, and I prove it
works by measuring it against a number I set *before* building it — not a number I picked
afterwards to look good.

**The flagship example, without the jargon.** The most widely used speech-recognition model
in the world is effectively unusable for Yoruba: it gets roughly 9 out of every 10 words wrong.
I measured that, then found a model that gets it down to about 3 in 10, and I published the
evidence — including the parts where my own attempts failed.

**Three terms you'll see here:**
- **WER (word-error rate)** — how often the model gets a word wrong. Lower is better.
- **Benchmark / baseline** — the existing system you're measuring yourself against.
- **Ship gate** — the pass mark I write down before I start, so the result can't be fudged.

Every number below links to the repository where you can check it.

---

## 🔬 Flagship — Aso Oke

**Closing the AI gap for Yoruba.** OpenAI's Whisper large-v3 scores a **92.6% word-error rate**
on Yoruba — essentially unusable for tens of millions of speakers.

I measured the baseline first, then built against it: a custom diacritic normalizer (a cleaner
that turns typed accents like "ọ̀" into plain letters so text can be compared reliably), a
per-dataset licence-audited data pipeline, and a **pre-registered ship gate** (the pass mark
written down before the work started).

The honest outcome is the interesting one — and it is two failures, not one:

| Model | FLEURS Yoruba test WER | Note |
|---|---|---|
| Whisper large-v3, no fine-tune | 92.6% | the floor |
| Whisper large-v3 + LoRA, 8 epochs | 61.4% | **my own fine-tune — failed the gate** |
| Omnilingual ASR LLM 1B, as-is | **32.0%** | zero Yoruba training — **cleared the ship bar** |

I chose the baseline over my own model, and documented exactly why. It also held up on unseen
local speakers (27.7% WER) and on women's voices (32.8%) — FLEURS' Yoruba test split is 100%
male, so that number did not exist until I measured it.

**The translator failed both of its own gates** and launches with a visible disclaimer rather
than as a polished feature: BLEU 11.7 / 8.0 against a pre-registered bar of 25 (BLEU is the
standard 0–100 score for translation accuracy), and a p95 of 7.4s against a 3s limit (p95
means 95% of requests finish faster than this). A cheap test on Nov 9 ruled out the obvious
suspect (beam search) and pointed at the 4-bit quantisation instead.

4.12s p95 latency on a single T4, a $400 hard compute ceiling ($149.95 spent so far), and a
public decision log.

→ [`github.com/donne4real/aso-oke`](https://github.com/donne4real/aso-oke) · [model adapter](https://huggingface.co/donne4real/aso-oke-madlad-lora) · ships 13 Dec 2026

---

## 🚀 Live demos

| Project | What it is | Link |
|---|---|---|
| **Bible in African Languages** | Bible reader that works with no internet connection, 22 translations, 45 tests | [bible-app.leyesapps.workers.dev](https://bible-app.leyesapps.workers.dev) |
| **Bible in African Languages — Google Play** | Published Android app, 50+ downloads. No data collected, nothing shared | [com.wordupafrica.biblereader](https://play.google.com/store/apps/details?id=com.wordupafrica.biblereader) |
| **NGX Tracker** | ~146 Nigerian Exchange stocks, tracked live | [ngx-tracker.pages.dev](https://ngx-tracker.pages.dev) |
| **Cert Mastery** | 300 questions each for AWS, Security+, CISSP, PMP, NCE, NCMHCE — the first three are the ones I'm certifying on | [cert-mastery.netlify.app](https://cert-mastery.netlify.app) |
| **Powerball Predictor** | Looks through 296 past lottery draws for patterns — hot numbers, 'due' numbers and pairs | [powerball-predictor.netlify.app](https://powerball-predictor.netlify.app) |
| **Exam Prep NG** | WAEC / NECO / JAMB practice questions across 12 subjects, checked automatically before every publish | [donne4real.github.io/exam-prep-ng](https://donne4real.github.io/exam-prep-ng/) |
| **PocketOffice** | Writer, Calc, Impress, text editor and PDF tools in a browser | [donne4real.github.io/PocketOffice](https://donne4real.github.io/PocketOffice/) |
| **Vocabulary App** | Vocabulary practice on a schedule that makes words stick | [build-my-vocab.netlify.app](https://build-my-vocab.netlify.app) |
| **Nia The Investigator** | Interactive investigation experience | [niatheinvestigator.netlify.app](https://niatheinvestigator.netlify.app) |

---

## 🧠 AI / ML work

| Project | What it is |
|---|---|
| [Aso Oke](https://github.com/donne4real/aso-oke) | Speech-to-text and translation for Yoruba, custom model tuning, pass marks set in advance |
| [DataInsight](https://github.com/donne4real/datainsight) | Offline local-LLM data analyst — 100% on-device, no API key |
| [Exam Prep NG](https://github.com/donne4real/exam-prep-ng) | Scripted curriculum pipeline generating question banks at scale |
| [MarketSage](https://github.com/donne4real/MarketSage-Analyzer) | Stock screener across 10 investment philosophies |

## 🛠 Engineering work

[Bible in African Languages](https://github.com/donne4real/bible-app) · [Cert Mastery](https://github.com/donne4real/cert-mastery) ·
[NGX Tracker](https://github.com/donne4real/ngx-tracker) · [PocketOffice](https://github.com/donne4real/PocketOffice) ·
[Powerball Predictor](https://github.com/donne4real/powerball-predictor) · [Vocabulary App](https://github.com/donne4real/vocabulary_app)

---

## 🧰 Toolkit

**AI/ML** — Python · PyTorch · PEFT/LoRA · Hugging Face · Transformers · Gradio · FastAPI · Flask · W&B
**Frontend** — React · TypeScript · Tailwind · Cloudflare Workers · JavaScript · PWA
**Data/Infra** — GitHub Actions · Cloudflare Pages · Netlify · R/Shiny · Databricks · SQL

---

## 🧭 How I work

- **Define the bar before you build.** Write the pass mark down first, then let the result decide.
- **Check the licence before you baseline.** Half my architecture calls on Aso Oke came from licence audits — one of them would have permanently blocked monetising the product if I'd found it at launch instead of in Week 1.
- **Say what doesn't work.** The model cards state the gaps as plainly as the wins.
- **Ship the boring parts too.** Automated checks that validate data before every build (CI/CD); 45-test suites; accessible, responsive UIs.

---

## 📍 Currently

- 🔨 **Building** — Aso Oke, shipping 13 Dec 2026
- 📜 **Certifying** — CISSP, Security+ and AWS, over the next year
- 📚 **Learning** — AWS AI & ML Scholars Nanodegree
- 🌍 **Based in** — Virginia, USA, working remotely

---

*Every number on this page is measured, not estimated. Source for all claims: the repositories above.*
