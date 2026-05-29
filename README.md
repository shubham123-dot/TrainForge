# TrainForge

**Build AI training datasets from any source — in your browser, in minutes.**

[**→ Open App**](https://shubham123-dot.github.io/TrainForge/) &nbsp;·&nbsp; No signup &nbsp;·&nbsp; No backend &nbsp;·&nbsp; Free with Groq

---

## What it does

TrainForge turns raw content into fine-tuning datasets for LLMs. Give it a Wikipedia article, a URL, a PDF, or pasted text — it generates instruction pairs, conversations, preference pairs, and adversarial examples ready to train on.

Built for ML engineers and researchers who want quality training data without the manual grunt work.

---

## Features

**5 generation pipelines**
- **Standard** — fast Q&A pairs from any source
- **Lab Quality** — 3-stage pipeline (concept extraction → targeted generation → polish pass), closest to what big labs produce
- **Adversarial** — trick questions, refusals, corrections, ambiguous prompts
- **Conversational** — realistic multi-turn with pushback, vague starters, follow-up chains
- **Persona Mix** — generates across 10 system prompt personas for diverse response styles

**Human Simulation engine**
Generates conversations that behave like real humans — frustrated, confused, anxious, impatient. Injects typos, vague openings, emotional outbursts, self-contradictions, late context dumps. Companies pay 3–5× more for realistic conversation data than plain Q&A.

**Automatic quality filters**
- Rejects sycophantic openers ("Certainly!", "Of course!", "Great question!")
- Rejects "as an AI" phrases
- Rejects context-dependent instructions ("in the provided text...")
- Rejects high-repetition responses
- Quality scores every example (0–100%)

**7 export formats**
OpenAI JSONL · HuggingFace JSON · Alpaca · ShareGPT · DPO/RLHF · CSV · Full backup

**Review workflow**
Approve/reject/regenerate individual examples. Keyboard shortcuts: `J`/`K` to navigate, `A` to approve, `R` to reject, `G` to regenerate.

---

## Getting started

1. Go to **[shubham123-dot.github.io/TrainForge](https://shubham123-dot.github.io/TrainForge/)**
2. Get a free API key from [console.groq.com](https://console.groq.com) (takes 30 seconds, no credit card)
3. Paste your key and click Start
4. Add a source → Generate → Review → Export

That's it. Your first dataset in under 5 minutes.

---

## Supported models

| Provider | Models | Cost |
|----------|--------|------|
| **Groq** | Llama 3.3 70B, Llama 3.1 8B, Mixtral 8x7B | Free tier available |
| **OpenAI** | GPT-3.5 Turbo, GPT-4o Mini, GPT-4o | Pay per token |

Groq is recommended — it's fast, free, and the Llama 3.3 70B model produces excellent training data.

---

## Export formats

| Format | Use case |
|--------|----------|
| `openai-finetune.jsonl` | Fine-tune GPT-3.5 / GPT-4o via OpenAI API |
| `hf-dataset.json` | Push to HuggingFace Hub with `push_to_hub()` |
| `alpaca-format.json` | Train LLaMA / Alpaca / Mistral models |
| `sharegpt-format.json` | Vicuna, multi-turn conversation training |
| `dpo-format.json` | DPO / RLHF preference pair training |
| `dataset.csv` | Review in Excel / Google Sheets |
| `trainforge-backup.json` | Full backup with all metadata |

---

## How to sell your datasets

TrainForge has a built-in **Sell** tab with step-by-step guides for:

- **HuggingFace Hub** — publish publicly or gated (free to list)
- **Gumroad** — sell directly, $10–$500 for niche datasets
- **Fiverr / Upwork** — custom dataset creation as a service, $100–$2,000/gig
- **B2B / Direct** — pitch AI startups directly, $500–$10,000+

It also generates listing copy for any platform using your dataset's actual stats.

---

## Running locally

It's a single HTML file. No build step, no dependencies, no server.

```bash
git clone https://github.com/shubham123-dot/TrainForge.git
cd TrainForge
open index.html   # or just double-click it
```

---

## Tech

- Vanilla HTML/CSS/JS — zero dependencies, zero frameworks
- Calls Groq or OpenAI APIs directly from the browser
- All data stored in `localStorage` — nothing leaves your machine except API calls
- Wikipedia API and allorigins.win CORS proxy for web scraping

---

## Roadmap

- [ ] Cloud save / sync across devices
- [ ] More source types (YouTube transcripts, PDFs, Notion pages)
- [ ] Dataset versioning
- [ ] Team collaboration
- [ ] More export formats (Dolly, OASST, Firefly)

Have a feature request? Open an issue.

---

## License

MIT — use it, fork it, build on it.

---

*Made with TrainForge · [shubham123-dot.github.io/TrainForge](https://shubham123-dot.github.io/TrainForge/)*
