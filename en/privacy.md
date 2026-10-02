---
title: "Privacy Policy"
lang: en
permalink: /en/privacy/
date: 2026-10-02
---

# Privacy Policy

Last updated: 2026-10-02

TectoWave - Android app.

## Who we are

This Privacy Policy applies to the TectoWave Android application ("the App"). The App is maintained by the TectoWave project, an independent developer. The App is not a government app and does not represent USGS, NOAA or any other government or political entity. Contact: alertsystems@atomicmail.io.

## Summary

- The App has no backend and no user accounts. No data from the App reaches a server we run, and we do not receive personal data from you.
- The App downloads public earthquake and tsunami data from USGS, EMSC, GEOFON and NOAA. These requests contain no personal data.
- Maps in the App are drawn by the Google Maps SDK. While a map is on screen, Google receives the map area shown, which can include the approximate centre of one of your watch zones or, in the zone map picker, your approximate current position when it has just filled in the zone's point (with "My location", or by itself on the "Your first place" page of setup). The SDK also sends Google its own technical data: device details, a pseudonymous SDK identifier, crash reports and map interactions. See "Google Maps" below.
- Everything else, including your watch zones and settings, stays on your device. The one exception is the language you pick on Android 13 and later, which Android keeps and may back up itself; see "On-device data".

## What we don't collect

- We do not run analytics, usage statistics or telemetry of our own. The Google Maps SDK collects usage and crash data for Google; see "Google Maps".
- We do not include crash reporting SDKs (Firebase Crashlytics, Sentry, Bugsnag, AppCenter: none).
- We do not include advertising SDKs, and the App does not use the advertising ID.
- We do not require accounts, login or any personal information from you.
- We do not offer in-app purchases.
- We do not collect user-generated content.
- We do not access your contacts, photos, files, calendar, messages, audio or other personal device data.

## Permissions and what they do

- **`INTERNET`** - to download earthquake data from USGS, EMSC and GEOFON, tsunami bulletins from NOAA, and maps from Google.
- **`ACCESS_NETWORK_STATE`** - to check connectivity, so that the background refresh runs only when a network is available.
- **`ACCESS_COARSE_LOCATION`** (optional, asked at runtime) - your approximate position, used to place a watch zone at your current position and to measure distances from where you are. The App gets it from Android's location service (Google Play services, under your device's location settings) and does not send it to us or to anyone else, with one exception: when your current position has just filled in a zone's point (with "My location", or by itself on the "Your first place" page of setup) and you open the zone map picker, the map opens on that approximate position, so Google receives that map area (see "Google Maps"). A zone created from it is saved like any other zone (see "On-device data"), and zone centres can be part of the map area Google receives (see "Google Maps").
- **`POST_NOTIFICATIONS`** (Android 13+, asked at runtime) - to show notifications that the App creates on your device. There are no remote push notifications.
- **`RECEIVE_BOOT_COMPLETED`** - to schedule the background refresh again after the device restarts. No data is sent.

## Network requests

The App makes HTTPS requests to the public data sources below: in the background about every 15 minutes while a network is available (Android may run this check less often to save battery, and after a failed check the App retries up to three times, waiting 5, 10 and 15 minutes between attempts), and when the App refreshes the feed. The requests contain no request body, no account, no user identifier and no location: only a start time and fixed options. Each request carries a User-Agent header with the App name, its version and the address of our contact page, so that data operators can reach us. The servers may log the IP address and User-Agent as part of normal operation; this is outside our control, and we do not receive those logs.

- **USGS** - public earthquake data from the U.S. Geological Survey, `https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/all_day.geojson`. USGS privacy policy: <https://www.usgs.gov/privacy>.
- **EMSC** - public earthquake records from the European-Mediterranean Seismological Centre event service at `https://www.seismicportal.eu`.
- **GEOFON** - public earthquake records from the GFZ GEOFON service (Potsdam) at `https://geofon.gfz.de`.
- **NOAA** - public tsunami bulletins from the U.S. tsunami warning centers (PTWC, NTWC) at `https://www.tsunami.gov`.
- **Google Maps** - map data for the maps in the App; see "Google Maps".

If sending your IP address to these public sources is a concern, you can use a VPN.

Fonts: the App asks Google Play services on your device for two fonts by name (Geist and JetBrains Mono). Google Play services downloads and caches them; the App passes only the font names and no data about you.

## Google Maps

The App uses the Google Maps SDK for Android, provided by Google LLC, to show maps in three places:

- the Map screen;
- the zone map picker, used to place a watch zone on a map;
- the small map at the top of an event's details screen. Tapping an earthquake notification opens this screen.

**Map area.** To draw a map, the SDK downloads map data for the area on screen, so Google receives that approximate area. The Map screen fits your watch zones and the listed events into view. The details map shows the event and, when your nearest watch zone is within 1,000 km of it, that zone's centre as well. The zone map picker opens on the zone's point, or on the whole world when there is none, and then shows the area you browse. That point can be your approximate current position, just filled in with "My location" or by itself on the "Your first place" page of setup; it is not rounded until the zone is saved. Zone centres are saved rounded to about 1.1 km, so the map area can show approximately where one of your watch zones is. The App does not turn on the map's "my location" layer.

**Data the SDK collects by itself.** Google documents that the Maps SDK for Android collects the following on its own, independently of the App's code (<https://developers.google.com/maps/documentation/android-sdk/play-data-disclosure>):

- request metadata: device OS version, name, model, brand and form factor, the SDK build and version, and an internal usage attribution identifier;
- stack traces and crash metrics when the SDK crashes;
- the IP address;
- a Maps SDK-specific pseudonymous identifier, used to count daily active users of the SDK;
- map interaction events, such as panning and zooming, because the App uses the map camera functions.

Google states that it uses this data to maintain and improve its services and the stability of the SDK. We do not receive any of it and cannot access or delete it. Google handles it under the Google Privacy Policy (<https://policies.google.com/privacy>); the maps are also subject to the Google Maps/Google Earth Additional Terms of Service (<https://maps.google.com/help/terms_maps/>).

The feed, settings and notifications do not show a map. If you do not open the Map screen, the zone map picker or an event's details, the App shows no map and sends no map area to Google.

## On-device data

- Cached public data (Room database): earthquake records from USGS, EMSC and GEOFON, deleted after about 26 hours, and NOAA tsunami bulletins.
- Your settings (Android DataStore and app preferences):
  - watch zones, the places the App notifies you about, up to 10: name, centre (rounded to about 1.1 km before it is saved), radius, minimum magnitude, and whether notifications are on;
  - the language chosen in the App (on Android 13 and later Android stores it as the App's language setting; see below);
  - whether onboarding was finished and whether the notification and location permission requests were shown;
  - the time of the last successful refresh and the tsunami bulletins you were already notified about.
- None of this is sent to us, and none of it leaves the device, except that zone centres can be part of the map area Google receives (see "Google Maps") and the language setting described in the next point.
- Android backup and device-to-device transfer are turned off for the App's data, so the list above is not copied to cloud backups or to a new phone. One exception: on Android 13 and later, the language you pick is kept by Android as the App's language setting (also shown in System Settings → Apps → TectoWave → Language), and Android's own backup of device settings can restore it on a new phone.
- Uninstalling the App removes all of this data.
- Manual reset: System Settings → Apps → TectoWave → Storage → Clear data.

## Links and sharing

Links you tap in the App (event pages, tsunami.gov, the USGS "Did You Feel It?" form, this policy) open in your browser, and the Share button hands the event text to the app you choose. When you have watch zones, that text includes the distance from your nearest watch zone and that zone's name. Those sites and apps have their own privacy policies.

## Children's privacy

The App is not directed to children under 13 (or the equivalent age in your jurisdiction). The App has no accounts and no data flows specific to children; all data that leaves the device is described in "Network requests" and "Google Maps".

## Changes to this policy

We may update this policy. The "Last updated" date at the top shows the most recent material change. Material changes are also mentioned in the Google Play release notes.

## Contact

Questions about this policy: alertsystems@atomicmail.io.

Contact page, also for data-source operators: <https://k41r05-a.github.io/tectowave-legal/contact/>.
