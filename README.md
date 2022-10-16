# Dynamic Playlist Creator - BETA

**Dynamic Playlist Creator** [^1] is a companion app for the *Dynamic Playlists 3* plugin. It helps you create dynamic playlists using templates.<br><br>
It is a **BETA** version because I expect bugs in the templates. **I don't use this plugin myself and don't have the time to test the templates against all possible parameter combinations**. And I won't release an untested plugin.<br><br>
If *enough* beta testers come forward to test the templates **extensively** (thank you!), perhaps one day this plugin can be part of the LMS plugin repository.
<br><br><br>


## Requirements
- the latest Dynamic Playlists 3 version

- LMS version ≥ 7.9

- LMS  database = SQLite. Preferably without major problems to avoid false positives.

- **GitHub account** for bug reports, discussion. **Everything** should be handled **on GitHub**, **not** the LMS forum. I'm just not there that much anymore.

- You agree to the usual beta disclaimer: You understand that this beta plugin probably contains bugs and is provided on an “as is” and “**as available**” basis without any express or implied warranty of any kind. You're advised to safeguard important data, to use caution and **not to rely in any way on the correct functioning or performance of this beta plugin**. In no event shall I be liable for any damages whatsoever arising out of the use of this plugin.
- Patience
<br><br><br>


## What to test for
Look for **template** bugs (in particular) by **creating dynamic playlists from each template**. Use *different* (combinations of) parameters for each dynamic playlist you create. Then play them with *Dynamic Playlists 3*. This beta is mainly about finding bugs, not about making feature requests.
<br>
Template bugs will usually give you sql errors (see server log) or result in tracks that do not (exactly) match your parameter selection.
<br><br><br>


## Report a bug
If you think that you've found a bug, open an [**issue here on GitHub**](https://github.com/AF-1/lms-dynamicplaylistcreator/issues) and fill out the ***Bug report* issue template**. Please post bug reports on **GitHub only**.<br>
<br><br><br>


## Installation

Add the repository URL below at the bottom of *LMS* > *Settings* > *Plugins* and click *Apply*:<br><br>
[**https://raw.githubusercontent.com/AF-1/lms-dynamicplaylistcreator/main/repo.xml**](https://raw.githubusercontent.com/AF-1/lms-dynamicplaylistcreator/main/repo.xml)
<br><br><br>


## Notes

- You can't import or migrate dynamic playlist definitions from the SQLPlayList plugin. The templates are different.
- Unlike SQLPlayList, DPLC will *always* save a fully “fleshed out” SQLite playlist, even if you use the recommended *Default format* (xml). That's because *Dynamic Playlists 3* scans the DPLC custom folder for **sql** files, i.e. how your dynamic playlists get listed in *Dynamic Playlists 3*.
- Compatible with *Dynamic Playlists 3*, *Custom Skip 3* and *Alternative Play Count*. CustomScan: untested.
- This plugin will not be localized because parameter names and value names are baked into the templates. And a halfway localized version is worse than a non-localized one.
<br>

[^1]:inspired by and based on Erland's SQLPlayList