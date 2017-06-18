# CubeScript Stuff

## Description
These scripts were written for fun and to add some things to Sauerbraten.  They are located in the folders for which they are intended whether it be for the WC-NG client, Remod server mod, or anything else.  With things involving chatbots, please refrain from being too spammy.  I have no control over what happens if you are kicked/muted/whatever for using some of these things inappropriately.

## Installation
### WC-NG or any other client-side scripts
1. Download the wanted .cfg file(s).
2. Move the file to the Sauerbraten directory.
3. (optional) Create "scripts" folder.  (I like to do this for organization.)
4. Open autoexec.cfg
5. Add `exec "FILNAME.cfg"` and save the file.  Use `exec "scripts/FILENAME.cfg"` if you did #3.

### Remod
1. Download the wanted .cfg file(s).
2. Place the file somewhere in the "scripts" directory of the Remod server.  (I recommend creating a folder for custom scripts.)
3. Open server-init.cfg
4. Add `exec "scripts/PATH-TO-SCRIPT.cfg"` then save the file.

Note: If the scripts require the use of the DB, I recommend specifying which database and table to use in the server-init.  The aliases will be given default values otherwise, and you can retrieve the names of the aliases (such as `login_db`) by looking in the first few lines of the scripts.
