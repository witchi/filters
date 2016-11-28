/**
 * Filters
 *
 * Plugin that adds a new tab to the settings section to create client-side e-mail filtering.
 *
 * @version 2.1.5
 * @author Roberto Zarrelli <zarrelli@unimol.it>
 * @developer Artur Petrov <admin@gtn18.ru>
 */


To install the plugin you have to:
1. PHP requirements: installed imap-module (--with-imap) for working with imap_mime_header_decode() function.
2. Download zip-archive to Roundcube/plugins folder;
3. Unzip downloaded zip-archive;
4. Rename unziped folder to 'filters';
5. Add "filters" in the plugins section of the roundcube configuration (config/config.inc.php).
For example:
$config['plugins'] = array(
 'archive',
 'password',
 'filters',
);

To setup the plugin, open the config.inc.php file and edit the following variables:
  $config['autoAddSpamFilterRule'] = TRUE;  // if TRUE a spam filter rule is created for all users which automatically move messages into junk folder  
  $config['spam_subject'] = '[SPAM]';       // How to mark the spam in the subject? To have effect the previous variable must be TRUE.
  $config['caseInsensitiveSearch'] = TRUE;  // if TRUE filters searching in case insensitive mode.
  $config['decodeBase64Msg'] = TRUE;        // if TRUE decodes base64 mail messages.


History

1.0 Initial version.
1.1 Fixed some important issues.
1.2 Fixed some minor issues - thanks to Marco De Vivo. 
1.3 Fixed some minor issues and added additional translations: Dutch and French - thanks to Ruud van den Hout.
1.4 News: each rule can now filter all, read or unread messages.
1.5 Fixed some important issues detected with Roundcube 0.8
1.6 Added additional translation: German - thanks to Fynn Kardel. 
1.7 Added additional translation: Russian - thanks to AresMax. 
1.8 Added additional translation: Czech - thanks to Miroslav Baka.
1.9 Added additional translation: Spanish - thanks to Yoni (MyRoundcube Dev Team - www.myroundcube.com). 
1.9.1 Added additional translations: Polish - thanks to Damian Wrzalski; Slovak - thanks to Miki.
1.9.2: 
  - Added additional translation: Portugal - thanks to antoniomr. 
  - Fixed the UTF-8 coding on the German translation - thanks to Veit.
  - Added the contrib section with third-party scripts.
  - Thanks to Carsten Schumann to write the manual filter patch for Filters 1.9.2 which adds the option to filter manually on request (i.e. to move all newsletters/alerts from inbox to trash).
    The patch expands the settings page with an option "Mode: automatic/manual" and adds a "manual filter" button to the toolbar. Finally, it updates the localization files.
2.0:
  - Added the 'auto add spam filter rule' which automatically add the rule to move messages into junk folder.
  - Added additional translations: Taiwan - thanks to Avery Wu;
  - Added additional translations: Romanian - thanks to Tache Madalin;
  - Fixed to UTF-8 the French translation - thanks to Nvirenque.
2.1:
  - Added the feature to filter base64 encoded mail messages;
  - Added the feature to filter messages searching in case insensitive or case sensitive mode;
  - Improved the code to prevent the javascript injection - thanks to Moritz;
  - Improved code organization;
  - Minor bug fixes.
2.1.1:
  - Fixed a bug which prevented to insert case sensitive search strings - thanks to Emanuele Bruno.
2.1.2:
  - Added a dynamic vertical scrollbar when there are a lot of filters to show - thanks to Alain Martini.
2.1.3:
  - Now check mail only in INBOX like yandex.mail or gmail;
  - fix "refresh" mailboxes after move mails;
  - Fixed a bug with the conflict rules. Add priority checkbox, now first rules with priority are working.
2.1.4:
  - Fixed for compare strings (Tested in all russian charset);
  - Fixed option: all, read and unread messages;
  - Added a new option: mark read or mark unread messages;
  - Fully replaced a search algorithm;
  - Fixed localization for 'folder' and 'folder.subfolder' - thanks to twisterbr;
  - Added additional translations: Japanese - thanks to tatsuyaueda;
  - Added config.inc.php;
  - Fix "decode and search BASE64 messages";
  - Added additional translations: Ukrainian - thanks to Dmitro Gnatoyko (dimagnatoiko@gmail.com).
2.1.5:
  - Fixed for Roundcubemail 1.2.2.
