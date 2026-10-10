# pr-reviewer

Workflow reutilizable que, en cada pull request, corre el CI del proyecto, revisa el diff con Claude Haiku 5.5 (via claude-code-action y suscripcion), aprueba o pide cambios, y manda el reporte por mail (Resend).

Cada repo lo usa con un archivo `.github/workflows/pr-review.yml` que llama a `francorep2/pr-reviewer/.github/workflows/review.yml@main`.

Secrets requeridos en cada repo: `CLAUDE_CODE_OAUTH_TOKEN`, `RESEND_API_KEY`.
