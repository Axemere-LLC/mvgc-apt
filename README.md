# Axemere APT Repository

The official Debian/Ubuntu **APT** repository for the **Axemere AI Gateway** by
[Axemere LLC](https://axemere.ai). It is served at **https://apt.axemere.ai**.

> ⚙️ **This repository is generated automatically** by our release pipeline
> (reprepro). Please **do not edit files here or open pull requests** — the package
> tree and its signatures are rebuilt on every release. Questions? See
> https://axemere.ai/docs.

---

## Install

The full setup — importing our signing key and adding the source — is documented in
one authoritative place, so you always get the current key and source line:

**https://axemere.ai/docs/guides/it-setup/linux-debian**

For reference, the repository is added as:

```bash
# Add the signing key
curl -fsSL https://apt.axemere.ai/gpg.key \
  | sudo gpg --dearmor -o /etc/apt/keyrings/mvgc.gpg

# Add the repository
echo "deb [signed-by=/etc/apt/keyrings/mvgc.gpg arch=$(dpkg --print-architecture)] \
  https://apt.axemere.ai stable main" \
  | sudo tee /etc/apt/sources.list.d/mvgc.list

sudo apt update && sudo apt install mvgc-gateway
```

> The docs are authoritative. If anything here differs from
> https://axemere.ai/docs/guides/it-setup/linux-debian, trust the docs.

## What is the Axemere Gateway?

An HTTP proxy between your applications and your AI providers: your provider keys
live in the gateway instead of your code, with real-time cost tracking, per-project
spend limits, usage attribution, policy controls, and a verifiable audit ledger.

Three ways to run it:

- **Free Gateway** — self-hosted, run anywhere, no account or request limits.
  → https://axemere.ai/docs/free-gateway
- **Self-Hosted Gateway** — your infra, connected to the Axemere Control Plane and
  Cloud Console. → https://axemere.ai/docs/guides/it-setup
- **Managed Gateway** — Axemere runs it in the cloud, no infra to operate.
  → https://axemere.ai/docs/guides/managed-gateway

## Links

- Product & docs — https://axemere.ai
- Debian/Ubuntu install guide — https://axemere.ai/docs/guides/it-setup/linux-debian
- Release artifacts — https://github.com/Axemere-LLC/mvgc-releases
