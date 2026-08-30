# Secure DNS in Brave

A concise, vendor-neutral configuration note for enabling DNS-over-HTTPS in Brave and verifying the resulting privacy and availability trade-offs.

> **Project status:** user guide; menu names and provider choices can change between Brave releases.

## What this repository contains

- Steps for opening Brave's security settings.
- Provider selection using Cloudflare as an example, not a requirement.
- Verification checks and troubleshooting guidance.
- A threat-model note explaining what encrypted DNS does and does not protect.

## Quick start

1. Open brave://settings/security in Brave.
2. Find Use secure DNS and enable it.
3. Choose a provider you trust or enter a custom DNS-over-HTTPS endpoint.
4. Visit the provider's diagnostic page and confirm encrypted DNS is active.
5. If resolution fails on a managed network, restore the previous setting and consult the network administrator.

## Engineering notes

- DNS-over-HTTPS encrypts DNS traffic between the browser and resolver; it does not hide destination IP addresses from the network.
- A custom resolver changes who can observe DNS queries, not whether observation exists.
- Enterprise policy, VPN software, parental controls, and captive portals can override or conflict with browser DNS.

## Repository map

| Path | Purpose |
| --- | --- |
| README.md | Configuration and threat-model guidance. |

## Safety and limitations

Do not bypass an organisation's network policy without authorisation. Choose a resolver based on jurisdiction, logging policy, filtering needs, and operational reliability—not only latency.

## Contributing

Open an issue before a large change. Keep changes focused, document assumptions, and include a reproducible verification step.

## License

MIT — see [LICENSE](LICENSE).
