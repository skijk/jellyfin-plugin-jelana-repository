# Jelana Jellyfin plugin repository

Add this URL in Jellyfin under Dashboard → Plugins → Repositories:

`https://raw.githubusercontent.com/skijk/jellyfin-plugin-jelana-repository/main/manifest.json`

## Jellyfin compatibility

| Jellyfin server | Jelana version | Download |
| --- | --- | --- |
| Jellyfin 12.0 or later | Jelana 0.2.x | Install the latest release from this repository catalog |
| Jellyfin 10.11.x | Jelana 0.1.25.0 | [Download Jelana 0.1.25.0 for Jellyfin 10.11](https://github.com/skijk/jellyfin-plugin-jelana-repository/releases/download/0.1.25.0/Jelana_0.1.25.0_jf10.11.11.zip) |

**Jelana 0.2.0.0 and later require Jellyfin 12 and cannot be installed on
Jellyfin 10.11.** Jelana 0.1.25.0 is the final compatible release for Jellyfin
10.11.x. The manifest retains both ABI generations so Jellyfin can select the
compatible version automatically.

## Dependencies and integrations

| Component | Status | Used for |
| --- | --- | --- |
| Jellyfin 12.0 | Required | Supported server and web client |
| Playback Reporting | Required | Playback event source |
| JS Injector | Optional | Adds Analytics to the Jellyfin 12 user menu, with a legacy Jellyfin 10 menu fallback |
| JellySpotlight | Optional consumer | Can display Jelana's cached trends on Home |

Jelana does not require File Transformation, JellySpotlight, JellyBulletin,
Arr Watch or the former standalone PHP application. Playback Reporting is
read only during Jelana's scheduled cache refresh; the UI reads Jelana's own
atomically replaced cache instead of querying Playback Reporting live.
