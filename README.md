# Business Plan for Serious Ben Entertainment

Serious Ben Entertainment Business Planning.

## Render Markdown

To render the Quarto document, use the following command in your terminal:

```bash
quarto render Businessplan.qmd
```

## Triggering automatic rendering on GitHub Pages

Add a Repository secret named `DISPATCH_TOKEN` with a PAT (personal access token) that has:
- Repository access: Only select repositories → DrBenjamin/DrBenjamin.github.io
- Repository permissions:
  - Contents: Read and write (required for repository_dispatch)
  - Actions: Read and write (often required for workflows to trigger off the event)
  - Metadata: Read‑only (default is fine)

To test the triggering of the workflow, you can use the following `curl` command in your terminal, replacing `TOKEN` with the actual value of your `DISPATCH_TOKEN` secret:

```bash
curl -i -X POST \
  -H "Accept: application/vnd.github+json" \
  -H "Authorization: Bearer TOKEN" \
  https://api.github.com/repos/DrBenjamin/DrBenjamin.github.io/dispatches \
  -d '{"event_type":"fetch_webpage","client_payload":{"source":"manual","sha":"manual","reason":"probe"}}'