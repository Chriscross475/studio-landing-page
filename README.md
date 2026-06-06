# Mycelium Gaming — studio landing page

The landing site for **Mycelium Gaming**, served at <https://asoma.duckdns.org/>.

It's an interactive **node-network**: a central hub with project orbs wired together by
mycelium threads. Hover a node for a glow + halo + a flowing-signal thread and an info
card; click to enter the project. A scroll-down **community** section invites people to
join, and **Super Castle Defenders** gets its own themed info page.

## Structure
- `index.html` — the node-network landing + community section. Self-contained: HTML, CSS,
  an ambient `<canvas>` mycelium backdrop, and vanilla JS that lays the nodes out in a ring
  (auto-balances as projects are added). No build step.
- `scd/index.html` — Super Castle Defenders info page (medieval/gold themed).

## The network
- **The Button** — live · `/button/`
- **Sandbox** — live · `/sandbox`
- **WeTube** — live · <https://wetube.duckdns.org>
- **Civ Cards**, **HypnoAI**, **Finance**, **Super Castle Defenders**, **More** — in progress

## Deploy
Static files served by Caddy on the Oracle box from `/var/www/studio`. No build — edit and copy:

```sh
scp index.html ubuntu@<host>:/var/www/studio/index.html
scp scd/index.html ubuntu@<host>:/var/www/studio/scd/index.html
```

🍄 built in the open
