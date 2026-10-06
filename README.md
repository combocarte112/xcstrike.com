<div align="center">

# XCSTRIKE API

**The Counter-Strike server list that only shows what's real.**
CS 1.6 · CS:S · CS:GO · CS2

[![Website](https://img.shields.io/badge/website-xcstrike.com-6574cd?style=for-the-badge)](https://xcstrike.com)
[![Server list](https://img.shields.io/badge/servers-live-5cb88a?style=for-the-badge)](https://xcstrike.com/servers)
[![Download CS 1.6](https://img.shields.io/badge/download-CS%201.6-c9a962?style=for-the-badge)](https://xcstrike.com/download-cs-16)
[![API](https://img.shields.io/badge/API-public-4bb1d4?style=for-the-badge)](https://xcstrike.com/tools/developers)

[Website](https://xcstrike.com) · [Server List](https://xcstrike.com/servers) · [Tools](https://xcstrike.com/tools) · [Download CS 1.6](https://xcstrike.com/download-cs-16) · [API Docs](https://xcstrike.com/tools/developers)

</div>

---

## What is XCSTRIKE?

[XCSTRIKE](https://xcstrike.com) is a home for the Counter-Strike community: a live server list for **CS 1.6, CS:S, CS:GO and CS2**, free tools for server owners, and a clean CS 1.6 client.

Most server lists are full of fake entries and padded player counts. On XCSTRIKE every new server is verified before it goes live, player counts come from live queries, and rankings come from real votes.

This repository documents the free **XCSTRIKE public API** and the **live server banners**, with ready-to-use examples.

## Public API

Free, read-only JSON API for server data. Full docs: **[xcstrike.com/tools/developers](https://xcstrike.com/tools/developers)**.

| Endpoint | Description |
|---|---|
| `GET /api/v1/server/{ip}/{port}` | One server, any game |
| `GET /api/v1/server/{ip}/{port}/players` | Players currently online |
| `GET /api/v1/server/{ip}/{port}/stats` | Player and uptime history |
| `GET /api/v1/{game}/servers` | Server list for one game (`cs16`, `cs2`, `csgo`, `css`) |
| `GET /api/v1/servers/batch` | Several servers in one request |
| `GET /api/v1/network/{slug}/servers` | All servers of a community network |

**Example:**

```bash
curl https://xcstrike.com/api/v1/server/93.119.104.200/25564
```

```js
const res = await fetch('https://xcstrike.com/api/v1/cs16/servers');
const data = await res.json();
console.log(data);
```

Please cache responses on your side: requests are rate-limited per IP.

## For players

- **[Live server list](https://xcstrike.com/servers)** with real player counts, maps, country flags and ping, for [CS 1.6](https://xcstrike.com/servers), [CS2](https://xcstrike.com/servers/cs2), [CS:GO](https://xcstrike.com/servers/csgo) and [CS:S](https://xcstrike.com/servers/css).
- **Monthly ranking:** vote for your favorite servers. Each month's winners earn a gold, silver or bronze crown.
- **[CS 1.6 XCSTRIKE Edition](https://xcstrike.com/download-cs-16):** Non-Steam, engine 8684 (NextClient), with **XCSCLIENT**, an in-game server browser that only lists real servers. No fake servers, no redirects, no adware.
- **[CheatDetector](https://xcstrike.com/cheatdetector):** prove you play clean with a quick PC scan.
- **[SteamID Finder](https://xcstrike.com/tools/steamid)**, **[CS2 Inventory](https://xcstrike.com/tools/cs2-inventory)**, **[Community Networks](https://xcstrike.com/networks)** and a community forum.

## For server owners

- **[Add your server](https://xcstrike.com/add-server)** for free. With 5 votes a month it also appears in the XCSCLIENT Internet list, and monthly winners get a spot in the client's Random Server.
- **Free cloud compilers**, nothing to install:
  - [AMXX Compiler](https://xcstrike.com/tools/amxx-compiler): `.sma` to `.amxx` for CS 1.6 (AMXX 1.8.2 / 1.9 / 1.10, custom `.inc` files)
  - [SourceMod Compiler](https://xcstrike.com/tools/sourcemod-compiler): `.sp` to `.smx` for CS:GO and CS:S
  - [CounterStrikeSharp Compiler](https://xcstrike.com/tools/cssharp-compiler): CS2 C# plugins without a local .NET SDK
- **Live banners** for forums and signatures: 5 styles (Wide, Slim, Hero, Mini, Card), themeable in Banner Studio, updated with your live player count.
- **Server Manager:** live in-game chat, web console, bans and stats from the browser, powered by the free XCSTRIKE server plugin.

## Server banners

Every server on XCSTRIKE gets live PNG banners. Replace `13` with your server ID (it's in your server's URL on xcstrike.com).

| Style | Size | URL |
|---|---|---|
| Wide | 560x95 | `https://xcstrike.com/banner/13-wide.png` |
| Slim | 350x25 | `https://xcstrike.com/banner/13-slim.png` |
| Hero | 650x135 | `https://xcstrike.com/banner/13-hero.png` |
| Mini | 250x110 | `https://xcstrike.com/banner/13-mini.png` |
| Card | 250x292 | `https://xcstrike.com/banner/13-card.png` |

Add `@2x` before `.png` for high-DPI screens (for example `13-mini@2x.png`).

**BBCode (forum signature):**

```bbcode
[url=https://xcstrike.com/server/13][img]https://xcstrike.com/banner/13-slim.png[/img][/url]
```

**HTML:**

```html
<a href="https://xcstrike.com/server/13" target="_blank">
  <img src="https://xcstrike.com/banner/13-mini.png"
       srcset="https://xcstrike.com/banner/13-mini@2x.png 2x"
       width="250" height="110" alt="Counter-Strike server on XCSTRIKE">
</a>
```

You can customize the colors of all your banners in **Banner Studio**, on your server page.

## Links

- Website: [xcstrike.com](https://xcstrike.com)
- Counter-Strike server list: [xcstrike.com/servers](https://xcstrike.com/servers)
- Free tools: [xcstrike.com/tools](https://xcstrike.com/tools)
- Download CS 1.6: [xcstrike.com/download-cs-16](https://xcstrike.com/download-cs-16)
- Community forum: [xcstrike.com/forum](https://xcstrike.com/forum)

---

<div align="center">

**[XCSTRIKE](https://xcstrike.com)** · Find servers · Compile plugins · Play clean

</div>
