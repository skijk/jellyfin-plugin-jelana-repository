# Jelana Jellyfin plugin repository

Add this URL in Jellyfin under Dashboard → Plugins → Repositories:

`https://raw.githubusercontent.com/skijk/jellyfin-plugin-jelana-repository/main/manifest.json`

Version 0.2.0.0 and later require Jellyfin 12.0. Jellyfin 10.11 servers must
use the retained 0.1.x releases. The manifest keeps both ABI generations so
Jellyfin can select a compatible version.

## Dependencies and integrations

| Component | Status | Used for |
| --- | --- | --- |
| Jellyfin 12.0 | Required | Supported server and web client |
| Playback Reporting | Required | Playback event source |
| JS Injector | Optional | Adds Analytics to the menu for regular users |
| JellySpotlight | Optional consumer | Can display Jelana's cached trends on Home |

Jelana does not require File Transformation, JellySpotlight, JellyBulletin,
Arr Watch or the former standalone PHP application. Playback Reporting is
read only during Jelana's scheduled cache refresh; the UI reads Jelana's own
atomically replaced cache instead of querying Playback Reporting live.
