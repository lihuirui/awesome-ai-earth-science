# Contributing / 贡献指南

Thanks for helping curate **Awesome AI Earth Science**.

## Rules / 规则

1. **Verified links only** — every Paper / Code URL must open (arXiv abs page or official GitHub). Do not invent titles, authors, years, or IDs.
2. **Entry format** — `- **Name** (Year) [[Paper](url)] [[Code](url)] — _optional one-line note_`
3. **Prefer official repos** — community mirrors only when the official code is unavailable; say so in the note.
4. **No fabricated metrics** — do not claim SOTA / score numbers unless citing a paper table with a link.
5. **Chinese + English** — section titles may be bilingual; keep model names in original English when that is the common form.

## Suggesting an entry / 提交条目

Open a PR that:

- adds the bullet under the correct taxonomy section in `README.md`
- optionally updates `data/entries.json` with `{name, arxiv, code, category}`

## Local checks / 本地检查

```bash
# spot-check a few links
curl -sI https://arxiv.org/abs/2212.12794 | head -1
```
