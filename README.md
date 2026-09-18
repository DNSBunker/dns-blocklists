[![License: GPL-3.0](https://img.shields.io/badge/License-GPL--3.0-blue.svg)](https://www.gnu.org/licenses/gpl-3.0.html)![GitHub last commit](https://img.shields.io/github/last-commit/hagezi/dns-blocklists)![GitHub issues](https://img.shields.io/github/issues/hagezi/dns-blocklists)![GitHub closed issues](https://img.shields.io/github/issues-closed/hagezi/dns-blocklists)![GitHub repo size](https://img.shields.io/github/repo-size/hagezi/dns-blocklists)[![shields.io Stars](https://img.shields.io/github/stars/hagezi/dns-blocklists)](https://github.com/hagezi/dns-blocklists/stargazers)

# :zap: DNS Blocklists

**Let's make the internet a nicer place!** Built with :heartbeat: for a safer, cleaner internet. It always looks impossible until someone just goes ahead and does it.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://cdn.jsdelivr.net/gh/hagezi/files@latest/assets/images/dark/hagezi-dns-blocklists.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://cdn.jsdelivr.net/gh/hagezi/files@latest/assets/images/light/hagezi-dns-blocklists.svg">
  <img src="https://cdn.jsdelivr.net/gh/hagezi/files@latest/assets/images/dark/hagezi-dns-blocklists.svg">
</picture>

DNS blocklists that block ads, trackers, telemetry, phishing, malware, scams, and other unwanted domains network-wide. They work for any region and with every common DNS server, ad blocker, and content blocker.

Like this project? If it's helped you out, drop a :star: (top right) and join the stargazers club! Every star genuinely helps.

---

## :rocket: Quick start <a name="quickstart"></a>

1. **Pick one main list.** [Multi PRO](#pro) fits most people. Not sure? See [which tier fits you](#choose).
2. **Add the [Threat Intelligence Feeds](#tif).** A security add-on that's worth running alongside any tier.
3. **Get your links.** The [Direct Link Generator](#linkgenerator) builds them for your app or device in one go. Prefer copying by hand? Check [which format you need](#formatguide) and use the tables below.
4. **Set it up.** Follow the [quick setup guide](FAQ.md#quicksetup).

Something blocked that shouldn't be, or the other way round? Look it up in the [Blocklist Lookup](#listlookup), then [report it](#support).

---

## :bookmark_tabs: Contents <a name="toc"></a>

| Section | Jump to |
|:--------|:--------|
| **Getting started** | [Quick start](#quickstart) · [Formats](#formatguide) · [Which tier fits you?](#choose) · [Setup guide](FAQ.md#quicksetup) · [Glossary](FAQ.md#glossary) |
| **Multi** (pick one) | [Overview](#overview) · [Light](#light) · [Normal](#normal) · [Pro](#pro) ([mini](#promini)) · [Pro++](#proplus) ([mini](#proplusmini)) · [Ultimate](#ultimate) ([mini](#ultimatemini)) |
| **Add-ons** | [All add-ons at a glance](#addons) |
| :lock: Security | [Threat Intelligence Feeds](#tif) ([medium](#tifmedium) · [mini](#tifmini) · [IPs](#tifips)) · [Fake](#fake) · [Pop-Up Ads](#popupads) · [DNS Rebind Protection](#dnsrebind) |
| :hammer_and_wrench: Hardening | [NRD/DGA](#nrd) · [DynDNS](#dyndns) · [Badware Hoster](#hoster) · [Most Abused TLDs](#tlds) · [URL Shortener](#urlshortener) |
| :no_entry_sign: Access restrictions | [DoH/VPN/Tor/Proxy Bypass](#bypass) ([complete](#bypass_all) · [DoH only](#bypass_dns) · [DoH IPs](#bypass_ips)) · [Safesearch not supported](#safesearch) · [Gambling](#gambling) ([medium](#gamblingmedium) · [mini](#gamblingmini)) · [Social Networks](#social) · [NSFW](#nsfw) · [Anti Piracy](#piracy) |
| :calling: Native trackers | [Amazon, Apple, Huawei, Microsoft, Samsung, TikTok, LG, Roku, Vivo, OPPO/Realme, Xiaomi](#native) |
| **Tools** | [Direct Link Generator](#linkgenerator) · [Blocklist Lookup](#listlookup) · [Cheat Sheet](CHEATSHEET.md) |
| **Using the lists** | [Update interval & mirrors](#mirrors) · [Recommended software](#recommendation) · [Online DNS services](#dnsservices) ([AdGuard DNS](#adguarddns) · [ControlD](#controld) · [HaGeZi DNS](#hagezidns) · [DNSBUNKER.org](#dnsbunker) · [Public RDNS](#publicrdns) · [RobinGroppe.de](#robingroppe) · [RethinkDNS](#rethinkdns) · [DNSwarden](#dnswarden) · [OpenBLD.net](#openbld)) |
| **Project** | [About](#about) · [Repository](#repository) · [Referral domains](#referral) · [Support](#support) · [FAQ](FAQ.md) · [Discussions](https://github.com/hagezi/dns-blocklists/discussions) · [Sources](sources.md) · [Disclaimer](#disclaimer) · [Contact](#contact) |

---

## :page_facing_up: Which format do I need? <a name="formatguide"></a>

Most lists are published in the same five formats. The blocked domains are identical in all of them, only the way they're written down changes, so pick the row that matches your tool.

| Format | Use it with |
|:-------|:------------|
| Adblock | Pi-hole, AdGuard, AdGuard Home, eBlocker, uBlock Origin, Brave (aggressive mode only), AdBlock-Fast, AdNauseam, Little Snitch Mini (smaller lists only) |
| DNSMasq | DNSMasq (v2.86 or newer), Diversion (v5 or newer) |
| Wildcard Asterisk | Blocky (v0.23 or newer), Nebulo, NetDuma, OPNsense, YogaDNS |
| Wildcard Domains | DNSCloak, DNSCrypt, FRITZ!Box (FRITZ!OS v8.40 or newer), TechnitiumDNS, adblock-lean, PersonalDNSfilter, InviZible Pro |
| RPZ | Bind, Knot, PowerDNS, Unbound, and other software supporting Response Policy Zones |

> [!IMPORTANT]
> :link: **Don't want to pick a format or copy links by hand? Use the [Direct Link Generator](#linkgenerator).** Select your app or device and it sets the format for you, then tick the lists you want and copy every download link in one go: [hagezi-mirror.dnsbunker.org/dlg.html](https://hagezi-mirror.dnsbunker.org/dlg.html)

A few lists can't be expressed the same way in every format, so their sections spell out what's available: [Most Abused TLDs](#tlds) (its own set of variants), [DNS Rebind Protection](#dnsrebind) (AdGuard only), [NRD/DGA](#nrd) (Adblock and plain domains only), and the IP lists for [TIF](#tifips) and [DoH](#bypass_ips).

The legacy Subdomains and Hosts formats live in a [separate repository](https://github.com/hagezi/dns-blocklists-legacy). Complete format-to-tool breakdown: [FAQ](FAQ.md#formats).

[:arrow_up: Back to contents](#toc)

---

## :books: Multi: the main lists <a name="overview"></a>

An all-in-one blocklist in five tiers that runs standalone and works for any region. It blocks ads, trackers, metrics, telemetry, fake sites, phishing, malware, scams, cryptojacking, and other junk. It's built on [various source blocklists](sources.md), but it isn't a pile of lists glued together: everything has been optimized and extended so it actually cleans up the internet across the board. How that works: [Which sources are used and how are the lists compiled?](FAQ.md#sources)

The tiers build on each other, so **pick exactly one**. They're named after cleaning tools: the bigger the tool, the more thoroughly it cleans, and the more likely it is to sweep up something you wanted to keep.

### :bar_chart: Main lists at a glance <a name="blocking-intensity"></a>

| List | Blocking type | Risk of breakage | Entries | Size-optimized<br>version |
|:--------|:--------------|:-----------------|--------:|-----------------------:|
| :green_book:[Light](#light)        | Relaxed             | Minimal          | 39661    | - |
| :blue_book:[Normal](#normal)       | Relaxed/Balanced    | Low              | 199045    | Light: 39661 |
| :ledger:[Pro](#pro)                | Balanced            | Low to moderate  | 229508      | Mini: 53522 |
| :orange_book:[Pro++](#proplus)     | Balanced/Aggressive | Moderate         | 254256  | Mini: 64046 |
| :closed_book:[Ultimate](#ultimate) | Aggressive          | High             | 279418 | Mini: 77370 |
| :closed_lock_with_key:[TIF](#tif)  | Threats only        | Low              | 2567731      | Medium: 858694<br>Mini: 186096 |

TIF works differently from the tiers: it's an add-on covering malware, phishing, and other live threats, and it's worth running alongside any tier. The size-optimized versions replace their full list, they're never added on top. Entry counts change with every build.

### :compass: Which tier fits you? <a name="choose"></a>

| Tier | Cleaning tool | Pick it if... |
|:-----|:--------------|:--------------|
| :green_book: [Light](#light) | Hand brush | your ad blocker chokes on big lists, or even Normal's low risk is too much |
| :blue_book: [Normal](#normal) | Broom | you want next to no breakage and nobody is around to unblock things |
| :ledger: [Pro](#pro) **(recommended)** | Big broom | you want solid ad blocking and good privacy with rare breakage, and someone can unblock the odd domain |
| :orange_book: [Pro++](#proplus) | Sweeper | you're an experienced user and ready to unblock things that break |
| :closed_book: [Ultimate](#ultimate) | Ultimate sweeper | you want maximum protection and know how to deal with breakage |

Using a browser extension, a mobile app, or a device with little RAM? Take the **mini** version of your tier ([Pro mini](#promini), [Pro++ mini](#proplusmini), [Ultimate mini](#ultimatemini)). For Normal, that's Light. Still unsure? See [which list version should I use](FAQ.md#whatshouldiuse).

### :jigsaw: What's included where <a name="inclusion-matrix"></a>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://cdn.jsdelivr.net/gh/hagezi/files@latest/assets/images/dark/inclusion-matrix.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://cdn.jsdelivr.net/gh/hagezi/files@latest/assets/images/light/inclusion-matrix.svg">
  <img src="https://cdn.jsdelivr.net/gh/hagezi/files@latest/assets/images/dark/inclusion-matrix.svg">
</picture>

The full inclusion matrix, including the standalone lists, is in the [Cheat Sheet](CHEATSHEET.md#inclusionmatrix).

---

### :green_book: Multi LIGHT: basic protection <a name="light"></a>

**Hand brush.** Cleans up the internet and protects your privacy without going overboard. Blocks ads, trackers, metrics, telemetry, and some badware. Basically a size-optimized Multi NORMAL, built only from domains that appear on Top 1M/10M lists (Umbrella, Cloudflare, Tranco, Chrome, BuiltWith, Majestic, DomCop).

> [!NOTE]
> Shouldn't cause any real restrictions. Crash reporters like Bugsnag, Crashlytics, Firebase, Instabug, and Sentry are only blocked from [Pro](#pro) upward.

| Entries | Adblock | DNSMasq | Wildcard<br>Asterisk | Wildcard<br>Domains | RPZ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 39661 | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/light.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/light.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/light.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/light-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/light.txt) |

---

### :blue_book: Multi NORMAL: all-round protection <a name="normal"></a>

**Broom.** Cleans up the internet and protects your privacy. Blocks ads, trackers, metrics, telemetry, phishing, malware, scams, fakes, cryptojacking, and other junk.

> [!NOTE]
> Mostly won't cause restrictions either, so it's a good pick if you don't have an admin handy to unblock anything. Crash reporters like Bugsnag, Crashlytics, Firebase, Instabug, and Sentry are only blocked from [Pro](#pro) upward.

| Entries | Adblock | DNSMasq | Wildcard<br>Asterisk | Wildcard<br>Domains | RPZ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 199045 | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/multi.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/multi.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/multi.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/multi-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/multi.txt) |

---

### :ledger: Multi PRO: extended protection (recommended) <a name="pro"></a>

**Big broom.** Cleans up the internet and protects your privacy. Blocks ads, trackers, metrics, telemetry, phishing, malware, scams, fakes, cryptojacking, and other junk.

> [!TIP]
> My personal go-to recommendation for solid ad blocking with good privacy without much hassle. Restrictions are rare, but it works best if you've got an admin nearby who can unblock something if needed.

**Referral links** (affiliate and tracking links): most still work. A handful get blocked anyway, mainly ones that double as regular trackers or are commonly tied to scam and spam links. [Details](FAQ.md#referral)

| Entries | Adblock | DNSMasq | Wildcard<br>Asterisk | Wildcard<br>Domains | RPZ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 229508 | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/pro.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/pro.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/pro.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/pro-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/pro.txt) |

#### :ledger: Multi PRO mini (best for browser/mobile ad blockers) <a name="promini"></a>

A size-optimized version for DNS or browser blockers and devices with limited RAM. Contains only the domains from the full Pro list that appear on Top 1M/10M lists (Umbrella, Cloudflare, Tranco, Chrome, BuiltWith, Majestic, DomCop).

| Entries | Adblock | DNSMasq | Wildcard<br>Asterisk | Wildcard<br>Domains | RPZ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 53522 | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/pro.mini.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/pro.mini.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/pro.mini.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/pro.mini-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/pro.mini.txt) |

---

### :orange_book: Multi PRO++: advanced protection (more aggressive) <a name="proplus"></a>

**Sweeper.** Cleans up the internet aggressively and protects your privacy hard. Blocks ads, trackers, metrics, telemetry, phishing, malware, scams, fakes, cryptojacking, and other junk.

> [!WARNING]
> The more aggressive sibling of Multi PRO. It might block a few legit domains by mistake, so it's best for experienced users. Ideally have an admin ready to unblock things that break.

**Referral links** (affiliate and tracking links): more get blocked than in Pro, specifically the ones that aren't used exclusively for link tracking. The bulk of the category still stays allowed. [Details](FAQ.md#referral)

| Entries | Adblock | DNSMasq | Wildcard<br>Asterisk | Wildcard<br>Domains | RPZ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 254256 | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/pro.plus.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/pro.plus.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/pro.plus.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/pro.plus-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/pro.plus.txt) |

#### :orange_book: Multi PRO++ mini <a name="proplusmini"></a>

Built the same way as [Pro mini](#promini), from the full Pro++ list. For DNS or browser blockers on limited hardware.

| Entries | Adblock | DNSMasq | Wildcard<br>Asterisk | Wildcard<br>Domains | RPZ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 64046 | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/pro.plus.mini.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/pro.plus.mini.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/pro.plus.mini.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/pro.plus.mini-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/pro.plus.mini.txt) |

---

### :closed_book: Multi ULTIMATE: maximum protection (most aggressive) <a name="ultimate"></a>

**Ultimate sweeper.** Strictly cleans up the internet and locks down your privacy. Blocks ads, trackers, metrics, telemetry, phishing, malware, scams, fakes, cryptojacking, and other junk.

> [!CAUTION]
> A stricter version of Multi PRO++. It contains domains that can limit app or website functionality, including some popular trackers that will cause hiccups. Only use this if you know what you're doing, and make sure someone can unblock things when needed.

<details>
<summary><b>Known side effects</b>: referral links, META apps, Windows/Xbox, location trackers</summary>

- **Referral links:** same as Pro++. Referral domains that aren't used exclusively for link tracking are blocked, the rest of the category stays allowed. [Details](FAQ.md#referral)
- **Facebook, Messenger, WhatsApp:** some META trackers are blocked, which limits Facebook and Facebook Messenger app functionality. WhatsApp's graph trackers are blocked too, which can mess with avatar creation, the in-app help center, and video effects. Other than that, WhatsApp works fine. If you use META apps, unblock these domains as needed: [META Tracker](share/facebook.txt)
- **Windows/Xbox:** some Microsoft trackers are blocked, which can affect things like Windows Spotlight and Xbox Live Achievements Activity History. Which domains to unblock for which feature: [Microsoft Tracker](share/microsoft.txt)
- **Location and IP trackers:** trackers that websites use to pin down your IP or location get blocked. Great for privacy, since they're usually used for hidden analytics and ad targeting, but it might trigger wrong regional settings, extra CAPTCHAs, or reduced site functionality here and there.
- **Anything else:** more known quirks are listed [here](share/ultimate-known-issues.txt).

</details>

| Entries | Adblock | DNSMasq | Wildcard<br>Asterisk | Wildcard<br>Domains | RPZ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 279418 | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/ultimate.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/ultimate.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/ultimate.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/ultimate-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/ultimate.txt) |

#### :closed_book: Multi ULTIMATE mini <a name="ultimatemini"></a>

Built the same way as [Pro mini](#promini), from the full Ultimate list. For DNS or browser blockers on limited hardware.

| Entries | Adblock | DNSMasq | Wildcard<br>Asterisk | Wildcard<br>Domains | RPZ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 77370 | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/ultimate.mini.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/ultimate.mini.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/ultimate.mini.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/ultimate.mini-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/ultimate.mini.txt) |

[:arrow_up: Back to contents](#toc)

---

## :heavy_plus_sign: Add-on lists <a name="addons"></a>

Add-ons go on top of your Multi tier. Some are already fully or partly contained in the higher tiers, so check the [inclusion matrix](CHEATSHEET.md#inclusionmatrix) before stacking them. The [Direct Link Generator](#linkgenerator) greys out anything your tier already covers.

:warning: can block legitimate sites or break things, read the section before enabling · :package: very large, needs a capable blocker or plenty of RAM

| Group | Add-on | Blocks | Heads-up |
|:------|:-------|:-------|:---------|
| :lock: [Security](#security) | [Threat Intelligence Feeds](#tif) | Malware, phishing, command-and-control, scams, cryptojacking | **Recommended for everyone.** :package: Medium and Mini versions for smaller blockers |
| | [Fake](#fake) | Fake shops, fake streaming sites, rip-offs, subscription traps | |
| | [Pop-Up Ads](#popupads) | Pop-up ads, from annoying to malicious | |
| | [DNS Rebind Protection](#dnsrebind) | Domains that resolve to private or local IPs | AdGuard only |
| :hammer_and_wrench: [Hardening](#hardening) | [NRD/DGA](#nrd) | Newly registered and algorithm-generated domains | :warning: :package: False positives, provided as-is without support |
| | [DynDNS](#dyndns) | Dynamic DNS services abused for phishing | |
| | [Badware Hoster](#hoster) | Hosters that keep serving badware through user uploads | :warning: Blocks whole providers, including legit sites |
| | [Most Abused TLDs](#tlds) | Entire top-level domains with a bad reputation | :warning: Legit sites on those TLDs get caught too |
| | [URL Shortener](#urlshortener) | Every known link shortener | :warning: Meant for high-security setups |
| :no_entry_sign: [Access restrictions](#restrictions) | [DoH/VPN/Tor/Proxy Bypass](#bypass) | Encrypted DNS, VPN, Tor, and proxy services | Needs firewall rules for ports 53 and 853 to be airtight |
| | [Safesearch not supported](#safesearch) | Search engines without Safesearch | |
| | [Gambling](#gambling) | Gambling sites | Medium and Mini versions for smaller blockers |
| | [Social Networks](#social) | Facebook, Instagram, TikTok, X, Snapchat, and others | Messengers and streaming platforms stay reachable |
| | [NSFW](#nsfw) | Adult content | |
| | [Anti Piracy](#piracy) | Sites and services for illegally distributing copyrighted content | |
| :calling: [Native trackers](#native) | [Native Tracker](#native) | Trackers built into devices and OSes, one list per vendor | Every tier already includes them at its own level |

---

## :lock: Security add-ons <a name="security"></a>

Lists that go after known threats and scams. Start with [TIF](#tif).

### :closed_lock_with_key: Threat Intelligence Feeds (TIF): a serious security boost (recommended) <a name="tif"></a>

Targets malware, cryptojacking, scams, spam, and phishing: domains known for spreading malware, running phishing attacks, and hosting command-and-control servers.

> [!WARNING]
> This list is huge and can eat up a lot of memory depending on your ad blocker. If that's an issue, grab the [medium](#tifmedium) or [mini](#tifmini) version instead. It's too big for the iOS AdGuard mobile app, and AdGuard Home needs at least 2 GB RAM. The RPZ version is split into two files because of its size, and you need both.

| Entries | Adblock | DNSMasq | Wildcard<br>Asterisk | Wildcard<br>Domains | RPZ<br>(split) |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 2567731 | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/tif.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/tif.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/tif.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/tif-onlydomains.txt) | :one: [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/tif-1.txt)<br>:two: [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/tif-2.txt) |

#### :closed_lock_with_key: TIF medium (best for browser/mobile ad blockers) <a name="tifmedium"></a>

Only the most important feeds, for ad blockers that struggle with the full list. Still too big for the iOS AdGuard mobile app, and AdGuard Home needs at least 1 GB RAM.

| Entries | Adblock | DNSMasq | Wildcard<br>Asterisk | Wildcard<br>Domains | RPZ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 858694 | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/tif.medium.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/tif.medium.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/tif.medium.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/tif.medium-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/tif.medium.txt) |

#### :closed_lock_with_key: TIF mini <a name="tifmini"></a>

A size-optimized version of TIF medium, for ad blockers that even struggle with that one.

| Entries | Adblock | DNSMasq | Wildcard<br>Asterisk | Wildcard<br>Domains | RPZ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 186096 | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/tif.mini.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/tif.mini.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/tif.mini.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/tif.mini-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/tif.mini.txt) |

#### :closed_lock_with_key: TIF IPs <a name="tifips"></a>

There's also an IPv4 version of this list, in [plain IP format](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/ips/tif.txt) for firewalls and [AdGuard Home format](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/tif-ips.txt), which extends the regular TIF list.

> [!TIP]
> If you use the IP list in AdGuard Home, it'll block any domain that resolves to a blocked IP. To stop domains from slipping through via IPv6, turn off IPv6 resolution in AdGuard Home:
> `Settings > DNS settings > DNS server configuration > Disable resolving of IPv6 addresses`

---

### :trollface: Fake: blocks scams, traps, and fake sites <a name="fake"></a>

Targets fake stores, fake streaming sites, rip-offs, subscription traps, and similar scams.

| Entries | Adblock | DNSMasq | Wildcard<br>Asterisk | Wildcard<br>Domains | RPZ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 17234 | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/fake.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/fake.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/fake.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/fake-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/fake.txt) |

---

### :tada: Pop-Up Ads: stops annoying and malicious pop-ups <a name="popupads"></a>

Targets pop-up ads that range from annoying to outright malicious.

| Entries | Adblock | DNSMasq | Wildcard<br>Asterisk | Wildcard<br>Domains | RPZ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 50556 | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/popupads.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/popupads.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/popupads.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/popupads-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/popupads.txt) |

---

### :shield: DNS Rebind Protection: stops attackers from pointing domains at your local network <a name="dnsrebind"></a>

Stops attackers from manipulating DNS responses so a domain points to a private or local IP address. This keeps malicious scripts from using DNS rebinding attacks to reach your internal network.

> [!IMPORTANT]
> Only works with AdGuard/AdGuard Home, and it's also selectable in AdGuard DNS. Other DNS blockers may already have their own rebind protection built in.
>
> Since it blocks anything resolving to a local IP, your internal hostnames might get caught too. In AdGuard, allowlist your local domains, something like: `@@||fritz.box^`

| Format | Link |
|:-------|:-----|
| AdGuard | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adguard/dns-rebind-protection.txt) |

[:arrow_up: Back to contents](#toc)

---

## :hammer_and_wrench: Hardening add-ons (use with care) <a name="hardening"></a>

These don't wait for a domain to show up in a threat feed. They block whole categories that attackers like to abuse: brand-new domains, dynamic DNS, badware hosters, shady TLDs, and link shorteners. That's effective, but most of them hit legitimate sites too. Read each warning before you enable anything here, and expect to maintain your own allowlist.

### :new: Newly Registered Domains (NRD/DGA) <a name="nrd"></a>

Newly registered domains are a favorite tool for threat actors running phishing, malware, and command-and-control operations, since they're easy to throw away and help dodge detection. There are two variants:

- **[NRDs](#nrd_all):** every newly registered domain, no filtering.
- **[Entropy NRDs/DGAs](#nrd_dga):** only newly registered domains with high entropy, meaning they were likely generated by a Domain Generation Algorithm (DGA). These look random and are commonly used by malware for resilient command-and-control channels.

> [!CAUTION]
> These lists are big and resource-heavy. They can spike memory usage and include false positives, since some legit domains are new too, so allowlist important services if needed. NRD lists come as-is, with no guarantees, no support, and no formal process for fixing false positives. Use them at your own risk.

> [!IMPORTANT]
> The base data comes from [Stamus Labs](https://www.stamus-networks.com/stamus-labs/subscribe-to-threat-intel-feed).
> Stamus Labs doesn't promise daily updates, so the data can sometimes lag by a few days.
>
> Current status of the data:
> - Stamus Labs: :green_circle: - Fri, 18 Sep 2026 04:31:46 UTC / 10763068 domains

#### :new: NRDs: all newly registered domains, unfiltered <a name="nrd_all"></a>

| Time<br>period | Entries | Format<br>Adblock | Format<br>Domains |
|:--------------:|--------:|:-----------------:|:-----------------:|
| 7 days ago to yesterday    | 3173785 | [Link](https://cdn.jsdelivr.net/gh/hagezi/nrd@latest/adblock/nrd7.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/nrd@latest/domains/nrd7.txt) |
| 14 days ago to 8 days ago  | 2933024 | [Link](https://cdn.jsdelivr.net/gh/hagezi/nrd@latest/adblock/nrd14-8.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/nrd@latest/domains/nrd14-8.txt) |
| 21 days ago to 15 days ago | 2332688 | [Link](https://cdn.jsdelivr.net/gh/hagezi/nrd@latest/adblock/nrd21-15.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/nrd@latest/domains/nrd21-15.txt) |
| 28 days ago to 22 days ago | 2406369 | [Link](https://cdn.jsdelivr.net/gh/hagezi/nrd@latest/adblock/nrd28-22.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/nrd@latest/domains/nrd28-22.txt) |
| 35 days ago to 29 days ago | 2933680 | [Link](https://cdn.jsdelivr.net/gh/hagezi/nrd@latest/adblock/nrd35-29.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/nrd@latest/domains/nrd35-29.txt) |

> [!NOTE]
> The five files are non-overlapping bands, so stack them for wider coverage: `nrd7` plus `nrd14-8` covers the last 14 days, add `nrd21-15` for 21 days, and so on.

> [!TIP]
> Besides the formats here, NRDs are also available elsewhere:
> - Wildcard (Asterisk): [Cebeerre/dnsblocklists](https://github.com/Cebeerre/dnsblocklists)

#### :capital_abcd: Entropy NRDs/DGAs: only high-entropy domains generated by DGAs <a name="nrd_dga"></a>

These domains are already part of the full NRD lists, just filtered down.

| Time<br>period | Entries | Format<br>Adblock | Format<br>Domains |
|:--------------:|--------:|:-----------------:|:-----------------:|
| Past 7 days    | 581230 | [Link](https://cdn.jsdelivr.net/gh/hagezi/nrd@latest/adblock/dga7.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/nrd@latest/domains/dga7.txt) |
| Past 14 days   | 1171373 | [Link](https://cdn.jsdelivr.net/gh/hagezi/nrd@latest/adblock/dga14.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/nrd@latest/domains/dga14.txt) |
| Past 30 days   | 2395038 | [Link](https://cdn.jsdelivr.net/gh/hagezi/nrd@latest/adblock/dga30.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/nrd@latest/domains/dga30.txt) |

---

### :lock_with_ink_pen: Dynamic DNS (DynDNS): guards against dynamic DNS abuse <a name="dyndns"></a>

Blocks dynamic DNS services that get abused for phishing campaigns and other shady activity.

| Entries | Adblock | DNSMasq | Wildcard<br>Asterisk | Wildcard<br>Domains | RPZ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 1537 | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/dyndns.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/dyndns.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/dyndns.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/dyndns-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/dyndns.txt) |

---

### :computer: Badware Hoster: guards against malicious hosting services <a name="hoster"></a>

Blocks known hosting providers that repeatedly host badware through user-uploaded content.

> [!CAUTION]
> This list blocks the root domains of hosting providers that keep showing up in threat feeds because of malicious subdomains, so legit sites hosted there get blocked too. That's overkill for most setups, though the trade-off can make sense in high-security environments. If you use it, you're on your own for unblocking any subdomains you actually need.

| Entries | Adblock | DNSMasq | Wildcard<br>Asterisk | Wildcard<br>Domains | RPZ | ControlD |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 1237 | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/hoster.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/hoster.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/hoster.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/hoster-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/hoster.txt) | [Link](https://github.com/hagezi/dns-blocklists/blob/main/controld/badware-hoster-folder.json) |

---

### :crystal_ball: Most Abused TLDs: blocks known shady top-level domains <a name="tlds"></a>

Blocks the most abused top-level domains, combining data from Cloudflare Radar, Netcraft, and SpamHaus.

> [!WARNING]
> This list blocks entire top-level domains (like *.top, *.shop, *.gdn) that have a bad reputation overall. Some legit sites get caught in the crossfire, but it's really effective against spam, scams, phishing, malware, and other garbage. Know what you're signing up for, and add anything you need to your personal allowlist.

<details>
<summary><b>Which domains get excluded, and why so few</b></summary>

Only well-known, reputable domains that show up on the supported top lists (Umbrella, Cloudflare, Tranco, Chrome, BuiltWith, Majestic, DomCop) or are essential for popular apps get considered for exclusion. Illegal domains, including piracy sites, stay blocked no matter what. Anything that doesn't clearly qualify gets reviewed case by case, and if there's no good reason to unblock it, it stays blocked.

This selective approach exists because AdGuard and uBlock Origin have technical limits on rule length when using denyallow/domain modifiers. Trying to exclude every legit domain would eventually break important rules, so exclusions have to stay limited and carefully picked.

</details>

The exclusion rules work differently from tool to tool, so this list comes in its own set of formats:

| Format | Link | Notes |
|:-------|:-----|:------|
| AdGuard | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/spam-tlds.txt) | For AdGuard and AdGuard Home |
| uBlock Origin | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/spam-tlds-ublock.txt) | For uBlock Origin and Adblock Plus |
| Adblock | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/spam-tlds-adblock.txt) | For Pi-hole and TechnitiumDNS. Spam TLDs with no exclusions |
| Adblock<br>(Aggressive)<br>+ Allowlist | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/spam-tlds-adblock-aggressive.txt)<br>[Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/spam-tlds-adblock-allow.txt) | For Pi-hole and TechnitiumDNS. Use both together |
| Wildcard<br>Domains<br>+ Allowlist | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/spam-tlds-onlydomains.txt)<br>[Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/spam-tlds-allow-onlydomains.txt) | For DNSCrypt. Use both together |
| RPZ | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/spam-tlds-rpz.txt) | Spam TLDs with no exclusions |
| RPZ<br>(Aggressive) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/spam-tlds-rpz-aggressive.txt) | All spam TLDs, matching the AdGuard and uBlock Origin versions |
| ControlD | [Link](https://github.com/hagezi/dns-blocklists/blob/main/controld/spam-tlds-combined-folder.json) | Importable ControlD folder |

---

### :link: URL Shortener: blocks link shorteners <a name="urlshortener"></a>

Blocks every known URL/link shortener out there.

> [!WARNING]
> Not really meant for everyday setups. Shorteners can hide where a link actually leads and help enable attacks, so blocking all of them makes the most sense in high-security environments. In lower-risk settings, being careful usually does the job. If you use this list, you're on your own for unblocking any domains you actually need.

| Entries | Adblock | DNSMasq | Wildcard<br>Asterisk | Wildcard<br>Domains | RPZ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 9965 | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/urlshortener.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/urlshortener.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/urlshortener.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/urlshortener-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/urlshortener.txt) |

[:arrow_up: Back to contents](#toc)

---

## :no_entry_sign: Access restrictions <a name="restrictions"></a>

These lists don't block threats. They restrict what people on your network can reach, which is useful when you filter a network for others, like family, guests, students, or employees. In that case, make sure your setup is legal where you are (see the [disclaimer](#disclaimer), "Your setup, your responsibility").

### :outbox_tray: DoH/VPN/Tor/Proxy Bypass: stops people from sneaking around your DNS <a name="bypass"></a>

Blocks common ways to bypass your DNS setup. It comes as three lists: **pick one of the first two**. The third is an IP-level companion to the DoH-only list, not to the complete edition.

> [!NOTE]
> To make sure your DNS server is actually the one being used, you'll need to redirect or block standard DNS traffic (TCP/UDP 53) and also block DNS over TLS/QUIC (TCP/UDP 853) outbound.

#### :outbox_tray: Complete edition: encrypted DNS servers, VPN, Tor, proxies <a name="bypass_all"></a>

| Entries | Adblock | DNSMasq | Wildcard<br>Asterisk | Wildcard<br>Domains | RPZ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 16432 | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/doh-vpn-proxy-bypass.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/doh-vpn-proxy-bypass.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/doh-vpn-proxy-bypass.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/doh-vpn-proxy-bypass-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/doh-vpn-proxy-bypass.txt) |

#### :outbox_tray: Encrypted DNS servers only <a name="bypass_dns"></a>

| Entries | Adblock | DNSMasq | Wildcard<br>Asterisk | Wildcard<br>Domains | RPZ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 3329 | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/doh.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/doh.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/doh.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/doh-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/doh.txt) |

#### :outbox_tray: Encrypted DNS server IPs <a name="bypass_ips"></a>

There's also an IPv4 version in [plain IP format](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/ips/doh.txt) for firewalls, and an [AdGuard Home format](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/doh-ips.txt).

> [!TIP]
> If you use the IP list in AdGuard Home, it'll block any domain that resolves to a blocked IP. To stop domains from slipping through via IPv6, turn off IPv6 resolution in AdGuard Home:
> `Settings > DNS settings > DNS server configuration > Disable resolving of IPv6 addresses`

---

### :mag: Safesearch not supported: blocks search engines that skip Safesearch <a name="safesearch"></a>

Blocks search engines that don't support Safesearch.

| Entries | Adblock | DNSMasq | Wildcard<br>Asterisk | Wildcard<br>Domains | RPZ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 203 | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/nosafesearch.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/nosafesearch.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/nosafesearch.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/nosafesearch-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/nosafesearch.txt) |

---

### :slot_machine: Gambling: blocks gambling content <a name="gambling"></a>

Blocks gambling-related sites.

| Entries | Adblock | DNSMasq | Wildcard<br>Asterisk | Wildcard<br>Domains | RPZ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 516980 | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/gambling.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/gambling.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/gambling.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/gambling-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/gambling.txt) |

#### :slot_machine: Gambling medium <a name="gamblingmedium"></a>

A medium-sized version for ad blockers that have trouble with the full gambling list.

| Entries | Adblock | DNSMasq | Wildcard<br>Asterisk | Wildcard<br>Domains | RPZ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 186245 | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/gambling.medium.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/gambling.medium.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/gambling.medium.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/gambling.medium-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/gambling.medium.txt) |

#### :slot_machine: Gambling mini <a name="gamblingmini"></a>

A size-optimized version of Gambling medium. Only contains domains that appear on Top 1M/10M lists (Umbrella, Cloudflare, Tranco, Chrome, BuiltWith, Majestic, DomCop).

| Entries | Adblock | DNSMasq | Wildcard<br>Asterisk | Wildcard<br>Domains | RPZ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 134081 | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/gambling.mini.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/gambling.mini.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/gambling.mini.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/gambling.mini-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/gambling.mini.txt) |

---

### :speech_balloon: Social Networks: blocks access to social networks <a name="social"></a>

Blocks social networks like Facebook, Instagram, TikTok, X (formerly Twitter), Snapchat, and others. Messaging apps like WhatsApp and streaming platforms like Twitch are not blocked, this list is strictly aimed at classic social networking sites.

| Entries | Adblock | DNSMasq | Wildcard<br>Asterisk | Wildcard<br>Domains | RPZ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 900 | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/social.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/social.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/social.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/social-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/social.txt) |

---

### :underage: NSFW: blocks adult content <a name="nsfw"></a>

Blocks adult content.

| Entries | Adblock | DNSMasq | Wildcard<br>Asterisk | Wildcard<br>Domains | RPZ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 74633 | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/nsfw.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/nsfw.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/nsfw.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/nsfw-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/nsfw.txt) |

---

### :skull: Anti Piracy: blocks piracy sites <a name="piracy"></a>

Blocks sites and services mainly used for illegally distributing copyrighted content.

| Entries | Adblock | DNSMasq | Wildcard<br>Asterisk | Wildcard<br>Domains | RPZ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 51171 | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/anti.piracy.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/anti.piracy.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/anti.piracy.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/anti.piracy-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/anti.piracy.txt) |

[:arrow_up: Back to contents](#toc)

---

## :calling: Native Tracker: blocks built-in trackers from devices, apps, and OSes <a name="native"></a>

Blocks the native trackers baked into devices, services, and operating systems that quietly track what you do.

> [!IMPORTANT]
> Every Multi tier already contains native trackers, at four increasing blocking levels. Pick the tier that matches how aggressive you want to be:
>
> - **Light and Normal:** the baseline. Only native trackers that won't break functionality, for a smooth experience.
> - **Pro:** blocks more than the baseline, while still staying out of your way.
> - **Pro++:** blocks nearly all of them, which might cause some restrictions or limit certain features.
> - **Ultimate:** blocks all native trackers, for max privacy.
>
> The lists below cover everything used to monitor user activity, so they can occasionally limit functionality. When you combine them with a Multi tier, you might need to manually unblock a specific tracker here or there.

| Device/Service | Adblock | DNSMasq | Wildcard<br>Asterisk | Wildcard<br>Domains | RPZ |
|:-------|:--------:|:--------:|:---------:|:--------:|:--------:|
| Amazon (Devices, Shopping, Video) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/native.amazon.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/native.amazon.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/native.amazon.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/native.amazon-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/native.amazon.txt) |
| Apple (iOS, macOS, tvOS) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/native.apple.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/native.apple.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/native.apple.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/native.apple-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/native.apple.txt) |
| Huawei (Devices) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/native.huawei.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/native.huawei.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/native.huawei.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/native.huawei-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/native.huawei.txt) |
| Microsoft (Windows, Office, MSN) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/native.winoffice.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/native.winoffice.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/native.winoffice.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/native.winoffice-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/native.winoffice.txt) |
| Samsung | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/native.samsung.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/native.samsung.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/native.samsung.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/native.samsung-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/native.samsung.txt) |
| TikTok (Fingerprinting) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/native.tiktok.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/native.tiktok.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/native.tiktok.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/native.tiktok-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/native.tiktok.txt) |
| TikTok (Fingerprinting) Aggressive | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/native.tiktok.extended.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/native.tiktok.extended.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/native.tiktok.extended.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/native.tiktok.extended-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/native.tiktok.extended.txt) |
| LG webOS | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/native.lgwebos.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/native.lgwebos.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/native.lgwebos.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/native.lgwebos-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/native.lgwebos.txt) |
| Roku | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/native.roku.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/native.roku.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/native.roku.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/native.roku-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/native.roku.txt) |
| Vivo | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/native.vivo.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/native.vivo.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/native.vivo.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/native.vivo-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/native.vivo.txt) |
| OPPO/Realme | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/native.oppo-realme.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/native.oppo-realme.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/native.oppo-realme.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/native.oppo-realme-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/native.oppo-realme.txt) |
| Xiaomi | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/adblock/native.xiaomi.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/dnsmasq/native.xiaomi.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/native.xiaomi.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/native.xiaomi-onlydomains.txt) | [Link](https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/rpz/native.xiaomi.txt) |

[:arrow_up: Back to contents](#toc)

---

## :wrench: Tools <a name="tools"></a>

### :link: Direct Link Generator: your download links in a few clicks <a name="linkgenerator"></a>

Rather not click your way through every list section on this page? **[hagezi-mirror.dnsbunker.org/dlg.html](https://hagezi-mirror.dnsbunker.org/dlg.html)** puts the links together for you:

1. Pick a source and a format, or just select the app or device you use and it sets the format for you.
2. Pick one Multi tier and tick the add-ons you want.
3. Copy the links at the bottom of the page one by one, or grab the whole set with **Copy all links**.

It's more than a typing shortcut, because it knows how the lists relate to each other:

- Anything your chosen tier already covers gets greyed out, and partial overlaps are spelled out instead of hidden.
- [NRD and DGA](#nrd) lock each other out.
- Picking the full [TIF](#tif) list in RPZ format hands you both of its files, so you can't end up subscribed to half of it.
- Lists that are unusually large, or powerful enough to cause trouble if you enable them blindly, carry a small badge.
- The source starts on the build mirror and can be switched to jsDelivr, GitHub, GitLab, or Codeberg, which also makes it an easy way to move an existing setup from one source to another.

> [!NOTE]
> It covers the [five standard formats](#formatguide) only, so the legacy Subdomains and Hosts formats aren't in there, and NRD, DGA, and the referral lists only show up in Adblock and Wildcard (Domains) format. [Most Abused TLDs](#tlds), [DNS Rebind Protection](#dnsrebind), the IP lists for [TIF](#tifips) and [DoH](#bypass_ips), and the ControlD folders follow their own naming scheme and are left out entirely, so use the link tables on this page for those. More detail in the [FAQ](FAQ.md#linkgenerator).

### :mag_right: Blocklist Lookup: check any domain or IP against every list <a name="listlookup"></a>

Not sure whether a domain is blocked, or which list is responsible for it? **[hagezi-mirror.dnsbunker.org/listseek.php](https://hagezi-mirror.dnsbunker.org/listseek.php)** answers both. Handy for hunting down a false positive, comparing what happens to a domain across tiers before you switch, or checking whether something is covered at all before you report it.

- **Input:** one entry or a whole batch, one per line, up to 50 per query. Domains and IPv4 addresses can be mixed, wildcard patterns like `*.example.com` work, and you can paste full URLs or bracketed notation (`example[.]com`) straight in.
- **Output:** a card per entry, listing every list that blocks it along with the exact rule.
- **Subdomain-aware:** look up `region1.app-measurement.com` and you'll see the match comes from `||app-measurement.com^`, a wildcard on the parent domain, not an entry for that exact hostname.
- **Follows CNAME chains** up to 8 hops, so a domain that isn't on any list itself still gets flagged if it points at something that is. The result shows the full chain.
- **Always current:** it reads the published lists straight from the build mirror, so results reflect the newest build.
- **NRD and DGA lists aren't searched by default.** They're very large and slow the search down noticeably, so switch them on only when you need them.

> [!NOTE]
> The Lookup reads the published lists, not your own setup, and it doesn't judge whether a domain is harmful. Your local allowlist, extra lists from other projects, or a copy that hasn't refreshed yet can all make your network behave differently. More detail in the [FAQ](FAQ.md#listlookup).

### :clipboard: Blocklists Cheat Sheet <a name="cheatsheet"></a>

A [quick reference table](CHEATSHEET.md) for every list at a glance, including the full [inclusion matrix](CHEATSHEET.md#inclusionmatrix).

[:arrow_up: Back to contents](#toc)

---

## :floppy_disk: Update interval & official mirrors <a name="mirrors"></a>

The lists are rebuilt several times a day, but not every source publishes every build. All four sources serve the same lists, they only differ in how often a finished build shows up:

| Source | What it is | Publishes |
|:---|:---|:---|
| [GitHub/jsDelivr](https://github.com/hagezi/dns-blocklists) | Reference repository | Once a day |
| [gitlab.com/hagezi/mirror](https://gitlab.com/hagezi/mirror) | Repository mirror | Once a day, in sync with GitHub |
| [codeberg.org/hagezi/mirror2](https://codeberg.org/hagezi/mirror2) | Repository mirror | Once a day, in sync with GitHub |
| [hagezi-mirror.dnsbunker.org](https://hagezi-mirror.dnsbunker.org) | Build mirror | Every build, roughly every 4 to 8 hours |

GitHub is the reference repository, and GitLab and Codeberg are its full mirrors, publishing one build per day in sync with it. The build mirror is connected directly to the build system and publishes every build as soon as it finishes.

> [!TIP]
> Once a day is plenty for most setups. If you want every build the moment it exists, use the build mirror at [hagezi-mirror.dnsbunker.org](https://hagezi-mirror.dnsbunker.org).

[:arrow_up: Back to contents](#toc)

---

## :bulb: Recommended software <a name="recommendation"></a>

**For network-wide DNS blocking:** [AdGuard Home](https://adguard.com), [Pi-hole](https://pi-hole.net/), [TechnitiumDNS](https://technitium.com/dns/), [Blocky](https://github.com/0xERR0R/blocky) (if you're comfortable with advanced setups), [adblock-lean](https://github.com/lynxthecat/adblock-lean) (for OpenWrt), or [eBlocker](https://eblocker.org/).

**Plus a browser content blocker:** DNS blockers do a great job protecting your privacy by cutting off trackers, metrics, and telemetry, and they block most ads, malware, scams, and fake sites. They can't catch everything, though, since some of that stuff doesn't work through DNS. That's why I **also** recommend pairing them with [AdGuard](https://adguard.com), [uBlock Origin](https://github.com/uBlockOrigin/), or [Ghostery](https://www.ghostery.com/) in the browser. For good content blocker filter lists, check out Yokoffing's [Recommended Filters for uBlock Origin](https://github.com/yokoffing/filterlists).

> [!TIP]
> :information_desk_person: [Still not sure which version to pick?](FAQ.md#whatshouldiuse)

[:arrow_up: Back to contents](#toc)

---

## :department_store: Online DNS services <a name="dnsservices"></a>

Don't run your own DNS server at home, or want protection for your phone when it's off your home network? These services have you covered. Exactly which lists are available where: [FAQ](FAQ.md#availablelists).

| Service | Cost | HaGeZi lists | Notes |
|:--------|:-----|:-------------|:------|
| [AdGuard DNS](#adguarddns) | Limited free, unlimited trial, paid | Normal to Ultimate, plus most add-ons | |
| [ControlD](#controld) | Free, paid | Light to Ultimate, TIF | Ready-made free endpoints per tier |
| [HaGeZi DNS](#hagezidns) | Free | Pro + TIF, or TIF only | EU: Germany/Finland, balanced blocking |
| [DNSBUNKER.org](#dnsbunker) | Free | Pro + TIF | EU: Germany, balanced blocking |
| [Public RDNS](#publicrdns) | Free | Aggressive family-safe set | EU: Finland, blocks NSFW, piracy, gambling too |
| [RobinGroppe.de](#robingroppe) | Free | TIF | EU: Germany, threat blocking |
| [RethinkDNS](#rethinkdns) | Free | Light to Ultimate, TIF, Bypass, DynDNS, Badware Hoster | Lists updated once a week |
| [DNSwarden](#dnswarden) | Free | Light to Ultimate, TIF | |
| [OpenBLD.net](#openbld) | Free | Pro + TIF | |

### AdGuard DNS <a name="adguarddns"></a>

On [AdGuard DNS](https://adguard-dns.io) (limited free, unlimited trial, paid) you can use:

- Normal, Pro, Pro++, Ultimate
- Threat Intelligence Feeds (TIF), Most Abused TLDs, Badware Hoster, DynDNS, DNS Rebind Protection, URL Shortener
- DoH/VPN/Tor/Proxy Bypass
- Gambling
- Anti Piracy
- Native Tracker (Apple, OPPO & Realme, Samsung, Vivo, Windows/Office, Xiaomi)
- NSFW (Parental Control > Block adult websites)
- Allowlist Referral

### ControlD <a name="controld"></a>

On [ControlD](https://controld.com) (free and paid) you can use Light, Normal, Pro, Pro++, Ultimate, and TIF.

<details>
<summary><b>Free endpoints</b>: DNS-over-HTTPS, DNS-over-TLS/QUIC, legacy DNS, and Apple profiles for every tier</summary>

| Blocklists | DNS-over-HTTPS | DNS-over-TLS/QUIC | Legacy DNS | Apple |
|:-----------|:---------------|:-------------|:-------------|:---:|
| Light | `https://freedns.controld.com/x-hagezi-light` | `x-hagezi-light.freedns.controld.com` | 76.76.2.37<br>76.76.10.37<br>2606:1a40::37<br>2606:1a40:1::37 | [Link](https://api.controld.com/mobileconfig/x-hagezi-light?type=free&exclude_common=1) |
| Normal | `https://freedns.controld.com/x-hagezi-normal` | `x-hagezi-normal.freedns.controld.com` | 76.76.2.40<br>76.76.10.40<br>2606:1a40::40<br>2606:1a40:1::40 | [Link](https://api.controld.com/mobileconfig/x-hagezi-normal?type=free&exclude_common=1) |
| Pro | `https://freedns.controld.com/x-hagezi-pro` | `x-hagezi-pro.freedns.controld.com` | 76.76.2.41<br>76.76.10.41<br>2606:1a40::41<br>2606:1a40:1::41 | [Link](https://api.controld.com/mobileconfig/x-hagezi-pro?type=free&exclude_common=1) |
| Pro Plus | `https://freedns.controld.com/x-hagezi-proplus` | `x-hagezi-proplus.freedns.controld.com` | 76.76.2.42<br>76.76.10.42<br>2606:1a40::42<br>2606:1a40:1::42 | [Link](https://api.controld.com/mobileconfig/x-hagezi-proplus?type=free&exclude_common=1) |
| Ultimate | `https://freedns.controld.com/x-hagezi-ultimate` | `x-hagezi-ultimate.freedns.controld.com` | 76.76.2.45<br>76.76.10.45<br>2606:1a40::45<br>2606:1a40:1::45 | [Link](https://api.controld.com/mobileconfig/x-hagezi-ultimate?type=free&exclude_common=1) |
| TIF | `https://freedns.controld.com/x-hagezi-tif` | `x-hagezi-tif.freedns.controld.com` | 76.76.2.46<br>76.76.10.46<br>2606:1a40::46<br>2606:1a40:1::46 | [Link](https://api.controld.com/mobileconfig/x-hagezi-tif?type=free&exclude_common=1) |

</details>

- **Paid:** check out Yokoffing's [ControlD Config Guide](https://github.com/yokoffing/Control-D-Config) for good settings.
- **Automation:** [controld-hagezi-sync](https://github.com/0x11DFE/controld-hagezi-sync) automatically syncs HaGeZi folder blocklists to ControlD profiles via API. Supports TOML config, dry-run mode, multi-profile mappings, and daily GitHub Actions syncs.

### HaGeZi DNS <a name="hagezidns"></a>

Free, non-commercial public resolvers for Europe (Germany/Finland), mixing privacy and security with minimal restrictions using the Multi Pro and Threat Intelligence Feed lists. More details in the [project repository](https://github.com/hagezi/dns-servers).

<details>
<summary><b>Pro + TIF resolvers</b> (Falkenstein, Nuremberg, Helsinki): ads, trackers, analytics, metrics, telemetry, phishing, malware, scams, fakes, cryptojacking</summary>

| Location           | Protocols     | Endpoint/URL                          | Apple<br>Config        | Recommended for    |
|--------------------|---------------|-------------------------------------|-----------------------|-------------------------|
| Germany, Falkenstein| DoH/DoH3      | `https://root.hagezi.org/dns-query`   | [Link](https://raw.githubusercontent.com/hagezi/dns-servers/refs/heads/main/mobileconfig/root-hagezi-org.mobileconfig) [QR](https://raw.githubusercontent.com/hagezi/dns-servers/refs/heads/main/mobileconfig/root-hagezi-org.mobileconfig.png)    | AT, BA, BE, BG, CH, CZ, DE, DK, FR, GB, HU, IE, IT, LU, NL, PL, RO, SI, SK |
|                    | DoT/QUIC      | `root.hagezi.org`                     |                       |                         |
|                    | Do53      | `188.34.161.210`<br>`2a01:4f8:c17:1c66::1` |                       |                         |
| Germany, Nuremberg| DoH/DoH3      | `https://wurzn.hagezi.org/dns-query`   | [Link](https://raw.githubusercontent.com/hagezi/dns-servers/refs/heads/main/mobileconfig/wurzn-hagezi-org.mobileconfig) [QR](https://raw.githubusercontent.com/hagezi/dns-servers/refs/heads/main/mobileconfig/wurzn-hagezi-org.mobileconfig.png)    | AT, BA, BE, BG, CH, CZ, DE, DK, ES, FR, GB, GR, HR, HU, IE, IT, LU, MD, MK, MT, NL, PL, PT, RO, RS, SI, SK, TR, UA |
|                    | DoT/QUIC      | `wurzn.hagezi.org`                     |                       |                         |
|                    | Do53      | `159.69.155.94`<br>`2a01:4f8:1c1c:d363::1` |                       |                         |
| Finland, Helsinki   | DoH/DoH3      | `https://juuri.hagezi.org/dns-query`  | [Link](https://raw.githubusercontent.com/hagezi/dns-servers/refs/heads/main/mobileconfig/juuri-hagezi-org.mobileconfig) [QR](https://raw.githubusercontent.com/hagezi/dns-servers/refs/heads/main/mobileconfig/juuri-hagezi-org.mobileconfig.png)    | DK, EE, FI, LT, LV, NO, SE |
|                    | DoT/QUIC      | `juuri.hagezi.org`                    |                       |                         |
|                    | Do53      | `95.217.163.17`<br>`2a01:4f9:c013:dc4e::1` |                       |                         |

</details>

<details>
<summary><b>TIF-only resolver</b> (Nuremberg): ONLY phishing, malware, scams, fakes, cryptojacking, and other harmful domains</summary>

| Location           | Protocols     | Endpoint/URL                          | Apple<br>Config        | Recommended for    |
|--------------------|---------------|-------------------------------------|-----------------------|-------------------------|
| Germany, Nuremberg| DoH/DoH3      | `https://ctif.hagezi.org/dns-query`  | [Link](https://raw.githubusercontent.com/hagezi/dns-servers/refs/heads/main/mobileconfig/ctif-hagezi-org.mobileconfig) [QR](https://raw.githubusercontent.com/hagezi/dns-servers/refs/heads/main/mobileconfig/ctif-hagezi-org.mobileconfig.png) | AT, BA, BE, BG, CH, CZ, DE, DK, ES, FR, GB, GR, HR, HU, IE, IT, LU, MD, MK, MT, NL, PL, PT, RO, RS, SI, SK, TR, UA |
|                    | DoT/QUIC      | `ctif.hagezi.org`                     |                       |                         |
|                    | Do53      | `162.55.58.40`<br>`2a01:4f8:1c19:6c19::1` |                       |                         |

</details>

### DNSBUNKER.org <a name="dnsbunker"></a>

[DNSBUNKER.org](https://dnsbunker.org/) is a free, hardened, privacy-first DNS resolver based in Germany (EU), with balanced blocking.

| Blocklists | DNS-over-HTTPS/3 | DNS-over-TLS/QUIC | Apple |
|:-----------|:---------------|:------------------|:--------|
| Pro + TIF | `https://dnsbunker.org/dns-query` | `dnsbunker.org` | [Link](https://dnsbunker.org/doh.mobileconfig) |

### Public RDNS <a name="publicrdns"></a>

[Public RDNS](https://public-rdns.com/) is a free, no-log recursive resolver in Finland (EU) for families. It uses HaGeZi lists to aggressively block ads, trackers, malware, NSFW content, piracy, gambling, and other unwanted domains. More info on the [project page](https://public-rdns.com).

### RobinGroppe.de <a name="robingroppe"></a>

[RobinGroppe.de DNS](https://www.robingroppe.de/serverzeug/dns-server) is a free, privacy-focused DNS service in Germany (EU). It doesn't log your queries and protects your connection by blocking malware, phishing, and other online threats using the HaGeZi Threat Intelligence Feeds.

### RethinkDNS <a name="rethinkdns"></a>

On [RethinkDNS](https://rethinkdns.com) (free) you can use Light, Normal, Pro, Pro++, Ultimate, TIF, Bypass, DynDNS, and Badware Hoster. Note that RethinkDNS only updates its lists once a week.

| Blocklists | DNS-over-HTTPS | DNS-over-TLS/QUIC |
|:-----------|:---------------|:-------------|
| Light + TIF | `https://sky.rethinkdns.com/1:AAkACAQA` | `1-aaeqacaeaa.max.rethinkdns.com` |
| Normal + TIF | `https://sky.rethinkdns.com/1:AAkACAgA` | `1-aaeqacaiaa.max.rethinkdns.com` |
| Pro + TIF  | `https://sky.rethinkdns.com/1:AAoACBAA` | `1-aafaacaqaa.max.rethinkdns.com` |
| Pro plus + TIF | `https://sky.rethinkdns.com/1:AAoACAgA` | `1-aafaacaiaa.max.rethinkdns.com` |
| Ultimate + TIF | `https://sky.rethinkdns.com/1:gAgACABA` | `1-qaeaacaaia.max.rethinkdns.com` |

### DNSwarden <a name="dnswarden"></a>

On [DNSwarden](https://dnswarden.com/customfilter.html) (free) you can use Light, Normal, Pro, Pro++, Ultimate, and TIF.

| Blocklists | DNS-over-HTTPS | DNS-over-TLS/QUIC |
|:-----------|:---------------|:------------------|
| Light + TIF | `https://dns.dnswarden.com/00000000000000000000048` | `00000000000000000000048.dns.dnswarden.com` |
| Normal + TIF | `https://dns.dnswarden.com/00000000000000000000028` | `00000000000000000000028.dns.dnswarden.com` |
| Pro + TIF  | `https://dns.dnswarden.com/00000000000000000000018` | `00000000000000000000018.dns.dnswarden.com` |
| Pro plus + TIF | `https://dns.dnswarden.com/0000000000000000000000o` | `0000000000000000000000o.dns.dnswarden.com` |
| Ultimate + TIF | `https://dns.dnswarden.com/0000000000000000000000804` | `0000000000000000000000804.dns.dnswarden.com` |

### OpenBLD.net <a name="openbld"></a>

[OpenBLD.net](https://openbld.net/docs/get-started/third-party-filters/hagezi/) (free) combines the Pro list with the TIF blocklist.

| Blocklists | DNS-over-HTTPS |
|:-----------|:---------------|
| Pro + TIF  | `https://ric.openbld.net/dns-query/hagezi` |

[:arrow_up: Back to contents](#toc)

---

## :loudspeaker: About <a name="about"></a>

<p align="center"><a href="https://github.com/hagezi/dns-blocklists/graphs/contributors"><img src="https://contrib.rocks/image?repo=hagezi/dns-blocklists&max=1" /></a></p>
<p align="center"><i><b>"If the plan doesn't work, change the plan, not the goal."<br>There's no place like 127.0.0.1!</b></i></p>

These blocklists are built on [various sources](sources.md) plus my own denylists and extensions. The goal has always been to avoid false positives as much as possible without giving up effectiveness, and dead entries get pruned regularly to keep the lists lean. So no, these aren't just random lists stitched together from other sources: they've been optimized and extended to genuinely clean up the internet across every category. Curious how? Check out: [Which sources are used and how are the lists compiled?](FAQ.md#sources)

**Benchmark.** While the lists were being developed, each version was tested against 10,000 websites from the Cisco Umbrella Top 1 million list: whether pages loaded properly, content displayed correctly, navigation worked, images loaded, videos played, and so on. All pages were opened and fully loaded in batch via Edge with privacy features turned off and cookies accepted, and cross-referenced through [whotracks.me](https://whotracks.me/websites.html). It was a one-off run, so the numbers are a snapshot, not live figures from the current build.

| **List**     | Total queries | Blocked queries | % blocked | % gap to light |
|-------------:|--------------:|----------------:|----------:|---------------:|
| **Ultimate** | 299646        | 131093          | 43.75     | 12.85          |
| **Pro++**    | 299646        | 119681          | 39.94     | 9.05           |
| **Pro**      | 299646        | 97508           | 32.54     | 1.65           |
| **Normal**   | 299646        | 93258           | 31.12     | 0.23           |
| **Light**    | 299646        | 92576           | 30.90     |                |
| **----**     | 299646        | 67888           | 22.66     | -8.24          |

Give it a try, share your feedback, and [report anything that should (or shouldn't) be blocked](https://github.com/hagezi/dns-blocklists/issues). Want to check a specific domain first? Use the [Blocklist Lookup](#listlookup).

### :octocat: Repository <a name="repository"></a>

The repository gets compressed (reinitialized) every now and then to keep its size in check. Heads up, this invalidates forks and wipes the commit history.

### :cyclone: Referral domains <a name="referral"></a>

Wondering how referral domains (affiliate and tracking links) are handled? Here's the answer: [FAQ on referral domains](FAQ.md#referral)

### :dizzy: Support <a name="support"></a>

This project only exists because of a genuinely supportive community. It's free for everyone and stays up to date thanks to ongoing care, updates, and contributions from people who actually want to make things better.

Feedback, ideas, domain reports, false-positive reports, whatever you've got, it's all appreciated. Every bit of help, big or small, makes the internet a little safer and cleaner for everyone.

Before you report a domain, run it through the [Blocklist Lookup](#listlookup). A report that names the exact list and rule is a lot quicker to act on. See: [Getting help and reporting issues](FAQ.md#support), or join the [Discussions](https://github.com/hagezi/dns-blocklists/discussions).

**Thanks for being part of this!**

[:arrow_up: Back to contents](#toc)

---

## :warning: Disclaimer <a name="disclaimer"></a>

The lists are provided free of charge, "as is," with no warranty of any kind. **By accessing, downloading, or using these DNS blocklists, you agree to be bound by the full disclaimer below.**

<details>
<summary><b>Read the full disclaimer</b>: scope, warranty, liability, your responsibility, third parties, availability, licensing, governing law</summary>

**Scope.** This disclaimer applies to these DNS blocklists and to the related lists published by the project, including the NRD/DGA lists and the legacy format lists (together, "the Lists"). The Lists are created and maintained by HaGeZi ("the Provider"). This disclaimer does not extend to any other service the Provider may separately operate (e.g., public DNS resolvers, the Blocklist Lookup, or the Direct Link Generator), which may be subject to its own terms.

**No warranty.** The Lists are provided free of charge, "as is" and "as available," with no warranty of any kind, express, implied, or statutory. The Provider makes no promises about accuracy, completeness, timeliness, reliability, or fitness for any particular purpose. There's no guarantee that every malicious or unwanted domain is covered, and no guarantee that legitimate domains won't get blocked by mistake. The Lists are compiled in part from third-party sources; the Provider does not control and is not responsible for errors originating in those sources.

**No accusation, no endorsement.** A domain showing up on a list is a technical filtering decision, not a legal finding and not a claim that whoever operates it did anything wrong. Categorization is based on third-party threat data, public rankings, and observed behavior, and any of that can be outdated or simply wrong. Brand names, domain names, and trademarks mentioned in the Lists or in this documentation belong to their respective owners and are used for identification only. If you operate a domain and think it's listed by mistake, ask for a review through the [issue tracker](https://github.com/hagezi/dns-blocklists/issues) or by mail at [support@hagezi.org](mailto:support@hagezi.org). Review and removal requests are handled on a best-effort basis, with no guaranteed response time.

**Assumption of risk.** Using the Lists is entirely at your own risk. The Provider disclaims any and all direct, indirect, incidental, or consequential liability for damages arising from using, misusing, or being unable to use the Lists, except where such damages result from willful misconduct or gross negligence on the Provider's part, or from death or personal injury caused by the Provider's negligence. Mandatory statutory liability that can't be excluded by agreement stays unaffected, whatever the wording above says.

**A supplement, not a substitute.** The Lists are meant to be one part of a broader defense-in-depth strategy, not the whole thing. They don't replace your own responsibility to do due diligence, run your own risk assessments, or use additional protections (firewalls, antivirus/EDR, IDS/IPS, etc.). There's no guarantee of compatibility with any specific system, platform, or setup. Nothing in the Lists or in the surrounding documentation is legal advice or professional security advice.

**Your setup, your responsibility.** You're responsible for making sure the way you deploy the Lists is legal where you are. That matters most when you filter a network other people use (family, guests, employees, students, customers) and when you use lists that restrict access rather than block threats, such as NSFW, Social Networks, Gambling, Anti Piracy, or the DoH/VPN/Tor/Proxy Bypass list. Employment, telecommunications, and data-protection rules can all come into play. The Provider offers no guidance on this and takes no responsibility for how the Lists are deployed.

**Third-party services and software.** DNS services, software, mirrors, and other projects linked or listed here are run by their respective operators, not by the Provider. Being mentioned is not an endorsement, and how those parties host, configure, delay, or modify the Lists is outside the Provider's control. Their own terms and privacy policies apply, including those of the platforms you download from (GitHub/jsDelivr, GitLab, Codeberg, and the build mirror).

**No guarantee of availability, fair use.** The Lists are a free, personal/community project, made available internationally, and no one is automatically entitled to their continued availability. The Provider may modify, suspend, restrict, or discontinue the Lists (in whole or in part) at any time and for any reason, including excessive query volume or abusive or disproportionate use, without notice and without liability, and is under no obligation to maintain, update, or continue providing them. The Provider makes reasonable efforts to fix faults once discovered, but does not guarantee any particular response or resolution time.

**Redistribution and licensing.** The Lists are published under the [GNU General Public License v3.0 (GPL-3.0)](https://www.gnu.org/licenses/gpl-3.0.html). A copy of the license is included in this repository and has to accompany any redistribution. You may redistribute, modify, and adapt the Lists only under the terms of that license. This disclaimer applies in addition to, and does not replace, the warranty and liability terms already contained in the GPL-3.0 (Sections 15 to 17). Some inputs come from third-party sources with their own licenses or terms of use. GPL-3.0 covers the Lists as published here; it doesn't hand you any rights in the upstream data itself, so if you build on that data directly, checking those terms is on you. It's on you to read, understand, and follow the license terms before using or redistributing anything.

**Governing law.** The Provider is based in Germany, and the Lists are made available for international use. This disclaimer is governed by the laws of Germany, without regard to conflict-of-law principles, to the extent permitted by applicable law. Nothing in this disclaimer limits any mandatory consumer-protection rights you may have under the law of your country of residence.

**Severability.** If any provision of this disclaimer is found invalid or unenforceable, the remaining provisions remain in full force and effect, and the invalid provision will be replaced by a valid one that most closely reflects its intended effect.

**Changes to this disclaimer.** The Provider may update this disclaimer from time to time. The version published alongside the Lists at the time of your access or use applies. Continued use of the Lists after an update constitutes acceptance of the updated disclaimer.

**Accepting these terms.** By accessing, downloading, or using these DNS blocklists, you agree to be bound by everything laid out in this disclaimer. If you do not agree, do not access, download, or use the Lists.

</details>

---

## :envelope: Contact <a name="contact"></a>

<div align="center">

[![Mail](https://img.shields.io/badge/Proton%20Mail-6D4AFF.svg?style=for-the-badge&logo=Proton-Mail&logoColor=white)](mailto:mail@hagezi.org)
[![Matrix](https://img.shields.io/badge/Matrix-000000.svg?style=for-the-badge&logo=Matrix&logoColor=white)](https://matrix.to/#/@hagezi:tchncs.de)
[![Signal](https://img.shields.io/badge/Signal-3B45FD.svg?style=for-the-badge&logo=Signal&logoColor=white)](https://signal.me/#eu/WlBfKuiT1S1GAGwDRpvIJErjM-C3IcjQUQ9HWLzeJKGKTfwlOGhEe7GQRSx05uX0)

</div>

---

<div align="center">

**Keep the internet clean!**

</div>

[![https://gafam.info](https://ptrace.gafam.info/unofficial/img/color/lqdn-gafam-poster-en-color-5x1-2560x.png)](https://gafam.info)
