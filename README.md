# cloudflared-mipsle

Builds of [cloudflared](https://github.com/cloudflare/cloudflared), the Cloudflare Tunnel client (formerly Argo Tunnel), for `linux/mipsle` (32-bit little-endian MIPS).

`cloudflared` is tunneling daemon that proxies traffic from the Cloudflare network to your origins. This daemon sits between Cloudflare network and your origin (e.g. a webserver). Cloudflare attracts client requests and sends them to you via this daemon, without requiring you to poke holes on your firewall --- your origin can remain as closed as possible.

Extensive documentation can be found in the [Cloudflare Tunnel section](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/) of the Cloudflare Docs.

## Binary

Each release has one statically linked `cloudflared` binary, cross-compiled from the latest cloudflared source with `CGO_ENABLED=0`. It doesn't depend on the system's libc.

## Building

Run **Actions → Build cloudflared for mipsle → Run workflow**. The workflow builds cloudflared's default branch and creates a release with the binary.
