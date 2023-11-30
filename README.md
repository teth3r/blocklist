# blocklist

Hardened config and blocklist for [dnscrypt-proxy](https://github.com/DNSCrypt/dnscrypt-proxy)

## Introduction

- `allowed-names.txt` this file bypasses domains blocked by `blocked-names.txt`.
- `blocked-names.txt` this file blocks websites by their domain names.
- `blocked-ips.txt` this file blocks websites by their ip addresses.
- `cloaking-rules.txt` this file matches domain names to ip addresses (useful for resolving captive portals).
- `dncrypt-proxy.toml` this file contains the configurations used by `dnscrypt-proxy`

## Features

- `server_names` = `starrydns`, `sby-limotelu`, `openinternet`, `dct-ru1`, `dct-de1`, `dct-nl1`, `dct-at1`, `ams-dnscrypt-nl`, `serbica`, `dnscrypt.be`, `sth-dnscrypt-se`, `dnscrypt.ca-1`, `dnscrypt.ca-2`, `scaleway-ams`, `scaleway-fr`, `techsaviours.org-dnscrypt`, `jp.tiar.app`, `altername`, `pryv8boi`, `deffer-dns.au`, `dnscrypt.pl`, `ffmuc.net` are the resolvers in use.

- `require_dnssec = true` (Require resolvers with support for DNS security extensions)

- `require_nolog = true` (Require resolvers to not log user queries)

- `require_nofilter = true` (Require resolvers that don't enforce their own blocklist)

- `log_level = 0` (Enable verbose logging)

- `dnscrypt_ephemeral_keys = true` (Creates a new, unique key for every single DNS query)

- `bootstrap_resolvers = ['45.11.45.11:53']` (Uses DNS.sb as the bootstrap resolver. Credits to [quindecim](https://github.com/quindecim))

- `netprobe_address = '45.11.45.11:53'` (use DNS.sb as netprobe address. Credits to [quindecim](https://github.com/quindecim))

- `doh_servers = false` (Require resolvers without the `DNS-over-HTTPS` protocol)

- `timeout = 2000` (Reduce the maximum response timeout of a single DNS query to `2000` ms)

- `blocked_query_response = 'refused'` (set `refused` response to blocked queries)

- `block_ipv6 = true` (Respond to IPv6 queries with an empty response)

- `anonymized_dns` (Use `routes` as an indirect way to reach DNSCrypt servers)

- `skip_incompatible = true` (Skip resolvers incompatible with anonymization)

- `direct_cert_fallback = false` (Prevent direct resolver fallback for failed updates of server certificates through a relay)

### Contributions

You can contribute to `allowed-names.txt` and `blocked-names.txt` at anytime by opening a new issue.
