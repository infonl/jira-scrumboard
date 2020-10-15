# jira-scrumboard
Tweaking the JIRA scrumboard. Creates a clear and concise JIRA scrumboard. Avoids the need to scroll all the time through your JIRA Scrum board so easier to show on a screen or share via videocall.

Requires a Chrome extension ("User JavaScript and CS"S) which allows you to inject your own JavaScript and CSS rules to any page, like your JIRA page. So this tweak does not require any change in JIRA, since it's not a JIRA plugin. See Install sequence below.

Active Sprints board
===========================
From the Active Sprints board there are several changes/features:
- Adapt the Active Sprints-board so more issues fit on. 
- Creates 2-1-1-2 columns instead of 1-1-1-1 and reduces the height of a card. Although the code is now aiming for a 4 column scrumboard, there is a 5 column option in comment so easy to implement.

Condensed High Contract-view (press Z multiple times). 
Optimal for larger screens for Daily Scrums/Daily standups.
- Creates 3-1-1-3 columns 
- Hides IDs, labels and priorities of subtasks: more space for titles + assignees
- Hides Details-pane to create a steady, non-moving screen while dragging 

Tips
- press Z to enable Fullscreen -> High contract (=condensed) -> Normal view -> Fullscren etc
- click on a card -> press A to assign people (type a part of then name and hit Enter twice)
- click on a card -> press . (dot) to choose any action (like Delete, Creating subtasks)
- Manually collapse rows of stories that are set to Done the day before to save space

Tips for exceptional cases
- For more zooming on even bigger screens: use Ctrl (or CMD) + or - (browser zoom)
- When in Condensed view: press Z to switch view and show/hide Details pane


Backlog view
=====================
From the Backlog-view there are several features:
- Create a copy-pastable list of issuetitles + links. Easy for in Slack/Mail (share list of stories that need refinement) and Powerpoint/Keynote (List stories in the Sprint Review presentation)
- Experimental: copy-pastable HTML blocks for adding a test-results table to Confluence/wiki

Howto
- Select a number of issues in the backlog view (use CMD/Ctrl of Shift to select multiple)
- Click on link called "show copyable list" on the right side of the Backlog-header to open a new tab with the name + link of each issues
(if this link doesn't show up: refresh the page)

Install
=====================
1. Download Zip from this repo (green button)
2. Unzip zipfile and extract user-js-css-v8-xxxxxx.json file 
3. install 'User JavaScript and CSS' extension for Chrome
https://chrome.google.com/webstore/detail/user-javascript-and-css/nbhcbdghjpllgmfilhnhkllmkecfmpld?hl=en
4. Click 'User JavaScript and CSS' icon in Chrome (Blue/red dotted lines-icon)
5. Go to Settings -> Settings
6. Choose 'Upload and Apply' under Backup if you did not use this plugin before
7. Select `user-js-css-v8-xxxxxx.json` file that you downloaded -> this should upload some settings and some css/js for your JIRA
8. If your JIRA url if different that this format: `jira.*/RapidBoard.jspa` (where * is a wildcard for any character): Edit the url under the Sites-tab -> should become your JIRA url, like `jira.yourdomain.com/jira/secure/RapidBoard.jspa`
9. Hit Save

Open your Active sprints-board in JIRA and hit refresh (F5).. and have fun!

NOTE: css.css and js.js are updated more frequently than the settings-file since that is easier to update for us. So we recommend updating your freshly installed version with the procedure below.

Update
=====================
To get the lastest version:
1. Go to your JIRA
2. Click 'User JavaScript and CSS' icon 
3. Open the two panes (js/css) in the plugin
4. Open https://raw.githubusercontent.com/infonl/jira-scrumboard/master/css.css And copy-paste content in the CSS pane. This will replace the old css.
5. Open https://raw.githubusercontent.com/infonl/jira-scrumboard/master/js.js And copy-paste content in the JS pane. This will replace the old js.
6. Save

Go to your JIRA and refresh page and have fun!

Happy paperless standups!

FAQ
===========================
*I don't see the nicer scrumboard. What is wrong?*
I asume you use Chrome and the extension and script installed via the procdure above. 
- Go to your JIRA.
- Click on the blue-red 'User JavaScript and CSS' extension icon in Chrome.
- Do you see a url under 'Rules for this page'?
- if not, click on the Settings-wheel icon of this extension
-- Do you see a url under Sites-tab?
--- if not: redo the install procedure above
--- if yes: you got in installed right, but the url is not correct 
--- click on the url in the list 
--- change the url to your JIRA url
- If you see a url under 'Rules for this page': make sure the toggle in front of it is green and make sure you refresh your JIRA-page.


