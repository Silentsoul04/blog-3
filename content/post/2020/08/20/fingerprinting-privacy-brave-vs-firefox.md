---
title: "Fingerprinting Privacy: Brave vs Firefox"
date: 2020-08-20T17:00:00-04:00
draft: false
url: "posts/fingerprinting-privacy-brave-vs-firefox"
categories:
- privacy
tags: 
- privacy
- web browser
- liberated
summary: "Brave and Firefox bill themselves as privacy champions. How do they fare at fingerprinting protection?"
---

[Brave](https://brave.com/rnr267 "Referrer link to download Brave")(Full
disclosure: that is a referrer link that will tell Brave I sent you) and
[Firefox](https://www.mozilla.org/en-US/firefox/ "Firefox Web Browser") both
bill themselves as privacy-championing browsers for consumers. I have a deep
appreciation for both projects: [Mozilla](https://www.mozilla.org/en-US/firefox/
"Mozilla organization")has been a champion of the open Internet for two decades,
and Brave is attempting to overthrow the incumbent revenue model of the
Internet.

In this post, I quickly compare the fingerprinting capability of these two
browsers by browsing to three fingerprinting demonstration sites:

* https://browserleaks.com/canvas (Canvas)
* https://audiofingerprint.openwpm.com/ (Audio)
* https://fingerprintjs.com/demo (FPJS)

I open each of these sites in a regular session and a private session for each
browser, then I reboot the browser and re-open each site in a regular and
private session for both browsers. Here's what I found:

> The desired outcome is for the browser hash to be unique on each visit to the
> page. A unique value on each page view means the tracking technology isn't
> able to trace back multiple sessions to one user.

| Firefox                  | Canvas Fingerprint | Audio Fingerprint | FPJS Fingerprint |
|--------------------------|--------------------|-------------------|------------------|
| Normal Session           | Unique - ✅        | Shared - 🚫       | Shared - 🚫      |
| Private Session          | Unique - ✅        | Shared - 🚫       | Unique - ✅      |
| Normal Session Reloaded  | Unique - ✅        | Shared - 🚫       | Shared - 🚫      |
| Private Session Reloaded | Unique - ✅        | Shared - 🚫       | Unique - ✅      |

| Brave                    | Canvas Fingerprint | Audio Fingerprint | FPJS Fingerprint |
|--------------------------|--------------------|-------------------|------------------|
| Normal Session           | Unique - ✅        | Unique - ✅       | Shared - 🚫      |
| Private Session          | Unique - ✅        | Unique - ✅       | Unique - ✅      |
| Normal Session Reloaded  | Unique - ✅        | Unique - ✅       | Shared - 🚫      |
| Private Session Reloaded | Unique - ✅        | Unique - ✅       | Unique - ✅      |
