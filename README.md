AutoRemovePlus
==============

AutoRemovePlus is a plugin for [Deluge](http://deluge-torrent.org) that you can use to automatically remove torrents.
Based on AutoRemove by Jamie Lennox, later AutoRemovePlus by Omar Alvarez.

This is a Gtk3UI and WebUI plugin.

Features
--------
- Select how many torrents are allowed at the same time.
- Choose to remove or pause them based on multiple criteria age, seeders, seed time, ratio or size.
- Set specific removal rules depending on tracker or label.
- Remove only torrents from specific trackers or labels.
- Only remove torrents if under a certain HDD space threshold.
- Select if torrents have to fulfill both or either criteria.
- Delete torrents in order (e.g. delete torrents with highest ratio first).
- Don't remove torrents if they don't reach a minimum time (in days), size or ratio.
- Choose the removal interval.
- Right click and select torrents that you don't want automatically removed.
- Remove torrent data option.
- Create an exempted tracker or label list, so that torrents that belong to those trackers or labels are not removed.
- Fully functional WebUI.
- Fully functional Gtk3UI.

Usage
-----
Look for torrents to remove every hour:

> Check interval: 1.00

Look for torrents to remove every day:

> Check every: 24.00

Remove every torrent that meets minimum criteria:

> Max. torrents: 0

Don't remove torrents unless Deluge has over 500:

> Max. torrents: 500

Remove torrents without checking free space:

> Minimum HDD space: -1

Only remove torrents when the main HDD has less than 10 GB free:

> Min. free space: 10

Remove torrents that have a ratio over 2.0 and have been seeding for at least 4 days:

> Remove by: Ratio, Min: 2.0, and, Remove by: Seed Time, Min: 4  

Remove torrents that have a ratio over 2.0 or have been seeding for at least 4 days:

> Remove by: Ratio, Min: 2.0, or, Remove by: Seed Time, Min: 4

Pause torrents instead of removing them:

> Uncheck the "Remove torrents" checkbox


The rest of the options are pretty self explanatory

Building
--------

Run:

```
python3 setup.py bdist_egg
```

The resulting `AutoRemovePlus-x-py3.x.egg` file can be found in the `/dist` directory.

Workarounds
-----------

If after building the egg file, the plugin does not load in Deluge:

- Delete the `AutoRemovePlus-x-py3.x.egg` in `/deluge/plugins` directory.
- Delete the `AutoRemovePlus.conf` files.
- Restart Deluge.
