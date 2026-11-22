# Jellyfin IPTV

Curated free US IPTV playlist + matching EPG guide for Jellyfin Live TV.

- `ackme-curated.m3u` — hand-picked channels: Utah local affiliates (CBS KUTV, Fox KSTU, BYU TV), weather, football/sports, racing, cop shows/crime, and daytime TV. Sourced from [iptv-org/iptv](https://github.com/iptv-org/iptv).
- `channels.xml` — channel list fed to the [iptv-org/epg](https://github.com/iptv-org/epg) grabber to produce `guide.xml`.
- `guide.xml` — generated XMLTV program guide, rebuilt daily by `.github/workflows/update-guide.yml`.

## Use in Jellyfin

Admin Dashboard → Live TV:

- **Tuner Device (M3U)**: `https://raw.githubusercontent.com/ack81/jellyfin-iptv/master/ackme-curated.m3u`
- **TV Guide Data Provider (XMLTV)**: `https://raw.githubusercontent.com/ack81/jellyfin-iptv/master/guide.xml`

3 channels have no EPG source available anywhere (Rally TV, True Crime Network, Classic TV Crime Drama) — they'll stream fine but show no program guide data.
