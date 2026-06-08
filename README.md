# SINK_JAIL IP Blocklist

A plain-text list of IP addresses currently held in a SINK_JAIL deployment —
IPs observed engaging in malicious or abusive behavior against the source network.

## Format

`sink_jail_blocklist.txt` — one IPv4 address per line, plain text. No headers,
no comments, no extra fields. Compatible with OPNsense's "URL Table (IPs)"
alias type and similar consumers — the same format used by Spamhaus DROP,
abuse.ch, FireHOL, and other community threat-intel feeds.

## Update frequency

Refreshed twice daily from the live source data.

## Subscribing (OPNsense)

Firewall → Aliases → add a new alias:

- **Type:** `URL Table (IPs)`
- **Content:** `https://raw.githubusercontent.com/orbit42/The-Zero-Day-Timeout-Corner/main/sink_jail_blocklist.txt`
- **Update Frequency:** your choice — this source changes at most twice daily
