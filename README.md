# Business Plan for Serious Ben Entertainment

Serious Ben Entertainment Business Planning.

## Render Markdown

To render the Quarto document, use the following command in your terminal:

```bash
quarto render Businessplan.qmd
```

## Triggering automatic rendering on GitHub Pages

curl -i -X POST \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: Bearer TOKEN" \
  https://api.github.com/repos/DrBenjamin/DrBenjamin.github.io/dispatches \
  -d '{"event_type":"fetch_webpage","client_payload":{"source":"manual","sha":"manual","reason":"probe"}}'