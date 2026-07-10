# senselight/skills

The content monorepo for senselight-fleet skills. Managed by `skill-server`
(the sole writer) and consumed by `skillctl` on developer machines.

## Layout

```
skills/<group>/<skill-name>/SKILL.md    — user-authored skills
vendored/<owner>/<repo>/<skill-name>/   — verbatim copies of 3rd-party skills
docs/                                    — content-repo documentation
```

## Tag pattern

`^(?<name>[a-z0-9][a-z0-9-]{0,79}(?:/[a-z0-9][a-z0-9-]{0,79})*)-v(?<semver>\d+\.\d+\.\d+)$`

Examples:
- `example/hello-world-v0.1.0` — a user skill `example/hello-world` at semver 0.1.0
- `security/audit-v1.2.3` — a user skill `security/audit` at semver 1.2.3

Only the server writes commits and tags. Do not push directly.

## Anti-usage

- No source code (this is a content repo)
- No secrets (`.env`, tokens, certs are `.gitignore`'d)
- No `node_modules/` (this repo has no build step)
