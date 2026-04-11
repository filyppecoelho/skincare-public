# skincare-public

Public data feed for the Skincare Alexa skill.

## Contents

- `rotinas.json` — skincare routines (calendar + steps per rotina) consumed by the Alexa-hosted Lambda.

## How it's updated

Auto-published daily at 4am (America/Sao_Paulo) by `daily_skincare.py` in the `personal-data` repo (private), via launchd.

## Why public

The Alexa-hosted Lambda needs an HTTPS endpoint to fetch routine data. Since it contains zero identifiable or sensitive info (just skincare product names, generic instructions, and a procedure calendar keyed by rotina A/B/C), a public repo is the simplest path.

## Consumers

- Alexa Skill (custom, hosted in the Amazon Developer account)
  - Invocation: `abra skincare`
  - Example: `Alexa, abra skincare Filyppe noite`
