# Awesome Generative Engine Optimization [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of tools, research, data and references for **Generative Engine Optimization (GEO)**: getting your product cited and recommended when buyers ask AI assistants like ChatGPT, Gemini and Perplexity for the best tool in a category.

Search moved. A growing share of buyers no longer type a query into Google and scan ten blue links. They ask an assistant, and the assistant hands back a short list of named products with a handful of cited sources. GEO is the practice of understanding how those answers get assembled, and getting your product into them.

This list favours things that are **measured and checkable** over opinion. Where a claim comes from a study, the study is linked so you can read the method and the limits yourself.

## Contents

- [Foundations](#foundations)
- [Tools: measure and monitor AI visibility](#tools-measure-and-monitor-ai-visibility)
- [Open data and studies](#open-data-and-studies)
- [AI crawlers reference](#ai-crawlers-reference)
- [Standards and machine-readable files](#standards-and-machine-readable-files)
- [Guides and playbooks](#guides-and-playbooks)
- [Communities](#communities)
- [Contributing](#contributing)

## Foundations

- [GEO: Generative Engine Optimization](https://arxiv.org/abs/2311.09735) — the paper that named the field (Aggarwal et al., 2023). Introduces the GEO benchmark and measures which content changes move a source up in a generative answer.
- [How AI answers get made: retrieval, not browsing](https://glotier.com/guides/where-ai-answers-come-from) — an assistant splits a question into smaller ones, retrieves a handful of sources it trusts, and writes from what it can parse.
- [GEO vs SEO](https://glotier.com/guides/geo-vs-seo) — the overlap and the difference: the work that gets a page retrieved by an assistant is largely the work that gets it ranked by Google.

## Tools: measure and monitor AI visibility

Products that measure whether assistants name you, track it over time, and show which sources feed the answers. Open a PR to add one.

- [Glotier](https://glotier.com) — affordable AI-visibility measurement across ChatGPT, Gemini and Perplexity, with a free page-level readiness check. Publishes its method and its own numbers. (Maintainer of this list, see disclosure below.)
- [Profound](https://www.tryprofound.com) — enterprise answer-engine analytics and monitoring.
- [Otterly.ai](https://otterly.ai) — AI search monitoring: mentions, links and sentiment across engines.
- [Scrunch AI](https://www.scrunch.com) — AI visibility and brand presence tracking for larger teams.

## Open data and studies

Original measurement, published with method and limits so it can be checked.

- [ai-visibility-data](https://github.com/oguzhanglotier/ai-visibility-data) — an open dataset of which sources AI actually cites in software categories, the AI-crawler identity landscape, model disagreement, and the one-slot-per-domain pattern in Google's AI answers. Raw counts, dated, with caveats.
- [What sources AI actually cites](https://glotier.com/guides/what-sources-ai-cites) — across 40 buying questions, community forums fed the answers far more than the review directories companies pay for.
- [How assistants disagree](https://glotier.com/guides/how-assistants-disagree) — handed identical sources, ChatGPT and Gemini agreed only about two thirds of the time on who to name, so a share of visibility is the model, not the source.
- [Who blocks AI crawlers](https://glotier.com/guides/who-blocks-ai-crawlers) — measured on the sites assistants actually cite, which ones let the crawlers in.

## AI crawlers reference

The user-agents that read the web on behalf of assistants. "Allowed" in your `robots.txt` is a permission you wrote down; "crawled" is an event in your logs. They are not the same, and only one shows up in your logs. A machine-readable version with operator IP-range files is in [ai-visibility-data](https://github.com/oguzhanglotier/ai-visibility-data).

| Operator | User-agent | Purpose |
|---|---|---|
| OpenAI | `GPTBot` | Training data collection |
| OpenAI | `OAI-SearchBot` | Decides what appears in ChatGPT search answers |
| OpenAI | `ChatGPT-User` | Fetches a page when a user asks about it |
| Anthropic | `ClaudeBot` | Training data collection |
| Anthropic | `Claude-User` / `Claude-SearchBot` | User-triggered fetch and search |
| Perplexity | `PerplexityBot` / `Perplexity-User` | Indexing and user-triggered fetch |
| Google | `Google-Extended` | Opt-out token for Gemini/Vertex training (not a crawler that fetches) |
| Google | `Googlebot` | Classic index, which also feeds AI Overviews |
| Apple | `Applebot` / `Applebot-Extended` | Search and the AI-training opt-out |
| Amazon | `Amazonbot` | Assistant and search data |
| Meta | `meta-externalagent` | Assistant and training data |
| ByteDance | `Bytespider` | Assistant and training data |
| Common Crawl | `CCBot` | Open crawl many models train on |

Note: a whole-site `Disallow` for the group matching an agent is a block; a path-only disallow is not, and parsers that miss the difference overstate blocking.

## Standards and machine-readable files

- [llms.txt](https://llmstxt.org) — a proposed `/llms.txt` file that gives models a curated, markdown map of your site.
- [Does llms.txt actually work](https://glotier.com/guides/does-llms-txt-work) — what the evidence does and does not show.
- [robots.txt](https://www.rfc-editor.org/rfc/rfc9309.html) — RFC 9309, the standard the AI crawlers above obey (or claim to).
- [Schema.org](https://schema.org) — JSON-LD structured data. Useful hygiene and classic-search discovery; its direct effect on AI citation is contested, so treat it as one signal, not a lever.

## Guides and playbooks

- [Generative Engine Optimization, explained](https://glotier.com/guides/generative-engine-optimization)
- [Why AI does not recommend you](https://glotier.com/guides/why-ai-doesnt-recommend-you)
- [Reddit and AI search](https://glotier.com/guides/reddit-and-ai-search) — why community threads punch above their weight in AI answers.
- [Rank in AI Overviews](https://glotier.com/guides/rank-in-ai-overviews)
- [How to verify AI-visibility data](https://glotier.com/guides/verify-ai-visibility-data) — what to demand of any vendor selling you a number, including us.

## Communities

- [r/SEO](https://www.reddit.com/r/SEO/) and its GEO threads.
- [Indie Hackers](https://www.indiehackers.com) — founders sharing what AI-search experiments actually moved.

## Contributing

Pull requests welcome. Add real, checkable resources. Prefer things with a method or a public artifact over marketing pages. One entry per line, alphabetical within a section where it makes sense, and a one-line honest description.

## Disclosure

This list is maintained by the team behind [Glotier](https://glotier.com), an AI-visibility tool. Glotier is listed alongside its competitors on the same terms, and entries are judged on whether they are useful and checkable, not on who made them. If a competitor belongs here and is missing, open a PR and it goes in.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the maintainers have waived all copyright and related rights to this work.
