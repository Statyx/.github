# Security Policy

## Scope

The repositories under this account are **demonstration and reference projects** for
Microsoft Fabric, Azure data services and Copilot-assisted engineering. They are
intended for learning, prototyping and customer demonstrations — not for production
use as-is.

## Reporting a vulnerability

Please **do not open a public issue** for security problems.

Use GitHub's private vulnerability reporting on the affected repository:
**Security** tab -> **Report a vulnerability**.

Expect an initial response within 5 business days.

## Reporting exposed credentials

If you find a credential, token, tenant ID, workspace ID or any other identifier
that appears to be real, please report it privately using the same channel. These
are treated with the same priority as vulnerabilities.

## What is out of scope

- Synthetic demo data. All datasets in these repositories are generated and fictional.
- Placeholder identifiers such as `00000000-0000-0000-0000-000000000000` or
  `<WORKSPACE_ID>`, which are intentional.
- Findings that require an already-compromised Azure tenant.

## Configuration guidance

These projects never commit real configuration. Every repository ships `*.example`
files that you copy locally:

```bash
cp src/config.example.yaml src/config.yaml
cp src/state.example.json  src/state.json
```

The real files are git-ignored. If a deployment script fails because an ID is
missing, that is intended behaviour — supply your own rather than reusing someone
else's tenant.