# California Fruit Sorting Quality Verifier

Render-ready web app for uploading sorting-quality packet PDFs and generating:

- AI verified PDF
- Issues CSV
- Trace JSON
- Cross-reference matrix XLSX
- Summary PNG

## Deploy On Render

1. Push this folder to GitHub.
2. In Render, create a new Blueprint from the repo.
3. Add this environment variable in Render:

```text
ANTHROPIC_API_KEY=your_claude_api_key
```

The free tier is configured in `render.yaml`. Uploaded/generated files are stored in `/tmp/sqr-verifier`, which is temporary on Render free tier.

The default Anthropic vision model is `claude-opus-4-20250514`, which was the most accurate model in testing for the sample packet. You can later change `ANTHROPIC_MODEL` in Render.

See `RENDER_DEPLOY.md` for more details.
