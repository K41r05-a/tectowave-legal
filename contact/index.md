---
title: Contact
permalink: /contact/
---

# Contact

TectoWave is an independent Android app that shows public earthquake
data from USGS, EMSC and GEOFON and tsunami bulletins from NOAA. It has
no backend: each installed copy reads the public feeds directly.

## For data-source operators

Requests from the app carry the User-Agent
`TectoWave/<version> (https://k41r05-a.github.io/tectowave-legal/contact/)`.
Each installation checks the feeds in the background at most every
15 minutes, and again when the user opens or refreshes the feed:
USGS `all_day.geojson`, the EMSC FDSN event service, the GEOFON event
list and the NOAA PTWC and NTWC Atom feeds. If this traffic causes a
problem, write to us and we will change the app in its next release.

## Everyone else

- Email: alertsystems@atomicmail.io
- Privacy Policy: [English](../en/privacy/), [Russian](../ru/privacy/)
- Public issues: https://github.com/K41r05-a/tectowave-legal/issues
