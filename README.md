# Dynamic Playlist Creator

**Dynamic Playlist Creator**[^1] (DPLC) allows you to create *custom* dynamic playlists for the *Dynamic Playlists* plugin using templates.<br>
The target group for this plugin is users who want to quickly and easily create custom dynamic playlists using **only** templates and **not** working directly with SQLite statements. Accordingly, DPLC does not include the option to edit SQLite statements manually (see FAQ).
<br><br>
[⬅️ **Back to the list of all plugins**](https://github.com/AF-1/)
<br><br><br>


## Requirements
- Dynamic Playlists version **4**

- LMS version ≥ 7.9

- LMS database = SQLite
<br><br><br>


## Screenshots
<img src="screenshots/dplc.gif" width="100%">
<br><br><br>


## Installation
⚠️ **Please read the [FAQ](https://github.com/AF-1/lms-dynamicplaylistcreator#faq) *before* installing this plugin.**<br>

You should be able to install **Dynamic Playlist Creator** from the LMS main repository (LMS plugin library):<br>**LMS > Settings > Plugins**.<br>

If you want to test a new patch that hasn't made it into a release version yet, you'll have to [install the plugin manually](https://github.com/AF-1/sobras/wiki/Manual-installation-of-LMS-plugins).

It usually takes a few hours for a *new* release to be listed on the LMS plugin page.
<br><br><br><br>


## Reporting a new issue

If you want to report a new issue, please fill out this [**issue report template**](https://github.com/AF-1/lms-dynamicplaylistcreator/issues/new?template=bug_report.md&title=%5BISSUE%5D+).
<br><br><br><br>


## FAQ

<details><summary>»<b>How do I <i>create</i> custom dynamic playlists?</b>«</summary><br><p>

- Go to <i>LMS home menu</i> > <i>Extras</i> > <i>Dynamic Playlist Creator</i> > <i>Create new dynamic playlist</i>.<br>

- Depending on the focus of your new dynamic playlist, <b>select a template</b>. The <i>Random Tracks - Advanced</i> template with its many options is a good starting point.<br>

- Enter a <b>name</b>, set the <b>parameters</b> you want to use and then <b>save</b> it. That's it.<br><br>

It <b>takes a couple of seconds</b> for the <i>Dynamic Playlists</i> plugin to start updating the list of available dynamic playlists and your new dynamic playlist to show up there. If you don't see your dynamic playlists listed, you can force a refresh of available dynamic playlists by (re)calling the <i>Dynamic Playlists</i> menu from the <i>LMS home</i> menu.
</p></details><br>

<details><summary>»<b>How can I <i>edit</i> custom dynamic playlists I've created with this plugin?</b>«</summary><br><p>
<i>Dynamic Playlist Creator</i> displays a list of all dynamic playlists that you have created with this plugin.<br>If you want to change the name of your dynamic playlist or some parameters, click on the <b>Edit</b> button next to the playlist's name, make your changes and save it. After a couple of seconds, the Dynamic Playlist plugin will update its list of available dynamic playlists and pick up the changes you just made.
</p></details><br>

<details><summary>»<b>Can I <i>edit the SQLite statement</i> of my dynamic playlists manually in DPLC?</b>«<br>&nbsp;&nbsp;&nbsp;&nbsp;»<b>What does the <i>export</i> button do?</b>«</summary><br><p>
The target group for this plugin is users who want to quickly and easily create custom dynamic playlists using <b>only</b> templates and <b>not</b> working directly with SQLite statements. Accordingly, DPLC does <b>not include the option to edit SQLite statements</b> manually in a tiny text area.<br><br>

Users familiar with SQLite can <b>use the <i>export</i> button</b> to <b>permanently move</b> a dynamic playlist <i>currently managed by DPLC</i> to the <i>Dynamic Playlists</i> plugin, i.e. its folder for custom dynamic playlists called <b>DPL-custom-lists</b>. There you can edit it like any other custom dynamic playlist with your favorite code editor.<br>
Moved dynamic playlists are removed from and no longer managed by DPLC.<br><br>Please note: the <b>export</b> button is <b>disabled by default</b> and can be enabled in DPLC's settings.
</p></details><br>

<details><summary>»<b>When I <i>edit</i> my custom dynamic playlist, DPLC displays a <i>saved version</i> number and a <i>new version</i> number. What does that mean?</b>«</summary><br><p>
When I change/add template parameters or fix template bugs, the template version number increases.<br>
If you created your custom dynamic playlist with a different/older template version than the current one, this discrepancy is displayed next to the template name on the edit page.<br><br>
<b>Updating</b> your custom dynamic playlist (recommended) is as simple as <b>saving it</b> again. Even if you don't change any parameter (value), this will make DPLC update the SQLite statement of your custom dynamic playlist.
</p></details><br>

<details><summary>»<b>What are the files in the <i>DynamicPlaylistCreator</i> folder for? Can I edit them?</b>«</summary><br><p>
When you create or edit and then <i>save</i> a custom dynamic playlist, DPLC will create 2 files in the <i>DynamicPlaylistCreator</i> folder (default location in the LMS playlists folder, can be changed in the plugin settings):<br>

- the file with the <b>customvalues.xml</b> extension contains the (template) values you selected for this dynamic playlist. It allows you to edit or update your custom dynamic playlist in DPLC at a later time.<br>

- In addition, DPLC will <b>always</b> save your custom dynamic playlist as an SQLite statement (file extension: <b>sql</b>) because <i>Dynamic Playlists</i> searches the DPLC custom folder for them.<br>

<b>⚠️ Do <u><i>not</i></u> move or edit any of these files manually!</b> DPLC will overwrite the changes. Or worse, your custom dynamic playlist will no longer work. And please <b>do not rename the <i>DynamicPlaylistCreator</i> folder</b>.
</p></details><br>

<details><summary>»<b>I can't set a <i>file</i> name for <i>new</i> dynamic playlists in DPLC anymore.</b>«</summary><br><p>
From version 1.<b>3.0</b> on, <b>DPLC handles all file names internally</b>. They are <b>derived from the <i>dynamic playlist name</i></b> and special characters are removed or replaced.<br>When you try to <i>save a new</i> dynamic playlist and DPLC finds a file with an identical file name, it will append a number to the end of the new file name so there will be no playlist ID conflicts. Once the dynamic playlist is saved, its <b>file</b> name (on which the playlist ID is based) won't change anymore, even if you change/edit the <b>playlist</b> name.
</p></details><br>

<details><summary>»<b>Why is the <i>Play button</i> not displayed for <i>all</i> dynamic playlists?</b>«<br>&nbsp;&nbsp;&nbsp;&nbsp;»<b>The <i>Play</i> button is not working for new dynamic playlists.</b>«</summary><br><p>
The <b>play</b> button is <b>disabled by default</b> and has to be enabled in DPLC's settings first.<br>
You can <b>only</b> start dynamic playlists directly in DPLC that do <b><u>not</u> ask for user input when started</b>. DPLC does not contain code to handle user-input parameters. To simplify the maintenance and updating of the plugin, I decided to create DPLC as a sort of dynamic playlist construction kit without duplicating any code from the <i>Dynamic Playlists</i> plugin.<br><br>After you have created a <b>new</b> dynamic playlist that does not ask for user input, please wait a few seconds before you try to start it with the <i>Play</i> button. <i>Dynamic Playlists</i> needs a moment to update the list of available dynamic playlists.<br><br>Starting dynamic playlists without user-input parameters in DPLC is just a quick way to test a dynamic playlist. The <i>Dynamic Playlists</i> plugin is still where you start your mixes, not DPLC.
</p></details><br>

<details><summary>»<b>Which plugins does DPLC work with?</b>«</summary><br><p>
It works with <a href="https://github.com/AF-1/lms-dynamicplaylists#faq"><b>Dynamic Playlists 4</b></a>, <a href="https://github.com/AF-1/lms-alternativeplaycount"><b>Alternative Play Count</b></a>, <a href="https://github.com/AF-1/lms-customskip#custom-skip"><b>Custom Skip 3</b></a> and <a href="https://github.com/AF-1/lms-customtagimporter#custom-tag-importer"><b>Custom Tag Importer</b></a>.
</p></details><br>

<details><summary>»<b>In some DPLC templates there's no option to set a <i>track limit</i> and no <i>do not repeat</i> setting.</b>«</summary><br><p>
Dynamic playlists that <b>use the LMS cache</b> cannot have a track limit because <i>Dynamic Playlists</i> <b>4</b> will load <b>all</b> track IDs matching the active dynamic playlist's search parameters into the cache using a single initial database query. The cached track ID list should not have duplicates, hence no <i>do not repeat</i> option. DPL 4 will add small batches of tracks from this cached list to the players's current playlist. The number of new unplayed tracks to be added per batch can be set in the DPL settings. It's a global setting for all dynamic playlists (except album dynamic playlists which should add complete albums).
</p></details><br>

<details><summary>»<b>Does DPLC handle online tracks?</b>«</summary><br><p>
DPLC creates dynamic playlists for the <i>Dynamic Playlists</i> plugin which will process <b>online tracks</b> that have been <b>added to your LMS library as part of an <i>album</i></b>. LMS does not import <b>single</b> online tracks or tracks of <i>online</i> <b>playlists</b> as <b>library</b> tracks and therefore these won't be processed by <i>Dynamic Playlists</i>.</p></details><br>

<details><summary>»<b>I <i>can't save</i> new dynamic playlists. I get this error message: “Could not create the <i>DynamicPlaylistCreator</i> folder“.</i></b>«</summary><br><p>
The <i>DynamicPlaylistCreator</i> folder is where DPLC stores all files related to your custom dynamic playlists and where the <i>Dynamic Playlists</i> plugin expects to find them. The folder name is hard-coded and must not be changed.<br>
On every LMS (re)start, DPLC checks if there's a folder called <i>DynamicPlaylistCreator</i> in the parent folder. The default <b>parent</b> folder is the <i>LMS preferences folder</i> but you can change that in DPLC's preferences. If it doesn't find the folder <i>DynamicPlaylistCreator</i> inside the specified parent folder, it will try to create it.<br><br>
The most likely cause for the error message above and matching error messages in the server log is that DPLC can't create the folder because LMS doesn't have read/write permissions for the parent folder (or the <i>DynamicPlaylistCreator</i> folder).<br><br>
So please make sure that <b>LMS has read/write permissions (755) for the parent folder - and the <i>DynamicPlaylistCreator</i> folder</b> (if it exists but cannot be accessed).
</p></details><br>

<details><summary>»<b>Can I import my custom dynamic playlists from the <i>SQLPlayList</i> plugin?</b>«</summary><br><p>
No, you <b>can't</b> import or migrate dynamic playlist definitions from the <i>SQLPlayList</i> plugin to <i>Dynamic Playlist <b>Creator</b></i>. They are based on templates which are different from the ones that DPLC uses.
</p></details><br>

<details><summary>»<b>Can I use <i>Dynamic Playlist Creator</i> and <i>SQLPlayList</i> at the same time?</b>«</summary><br><p>
<i>Dynamic Playlists</i> version <b>4</b> ignores SQLPlayList. There's no benefit but no harm either in keeping it installed.
</p></details><br>

<details><summary>»<b>Can you translate DPLC into my language?</b>«</summary><br><p>
This plugin will not be localized because parameter names and value names are baked into the templates. And a halfway localized version is worse than a non-localized one.
</p></details><br>
<br>

[^1]:inspired by and based on Erland's SQLPlayList