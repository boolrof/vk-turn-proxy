# Agent instructions

## Scope
This repository contains vk-turn-proxy application code and client/server routing helpers. Treat protocol/provider behavior and reachable TURN infrastructure as runtime facts that can change.

## Read first
1. `README.md`
2. task-relevant client/server code and workflow files

## Before changes
- Inspect branch/status/diff and preserve unrelated work.
- Verify protocol mode, target platform and current runtime behavior before changing routing/proxy logic.
- Never commit real private keys, credentials, tokens, production WireGuard configs or private infrastructure secrets.

## Change policy
- Keep example keys/addresses as placeholders.
- Do not change host/client routes, firewall or production service state merely to test source changes without explicit authorization.
- Provider/TURN endpoints found in docs are observations/examples, not guaranteed current inventory.
- New dependencies/protocol changes require source/version/compatibility review.

## Verification
- Run Go build/tests for affected packages and platform-specific script checks where applicable.
- Test the affected transport mode in an isolated/bounded setup.
- Verify route changes are limited to the intended traffic and have a restoration path.
- Review final diff for secrets and generated artifacts.

## Rollback
Use Git for code rollback. For route/runtime experiments, capture the pre-change routing state and restore it explicitly if validation fails.
