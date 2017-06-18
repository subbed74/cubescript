# Remod Script Descriptions

## User system (mod_login.cfg)
This is a basic user system for name-protection.  It can use either the default SQLite database or a MySQL database.  A table is created on first-run to store the user information.  The script currently features two commands: #login, #register.

#### #login [USERNAME] [PASSWORD]
This will log a user in if the information provided is correct.  Users are able to login to their registered name under an alias assuming the alias being used is not protected.  When a logged in user disconnects, they will be logged out.  If a user connects under a protected name, they are muted and will remain muted until they login or change to an unprotected name.

#### #register [PASSWORD]
This command registers a user using the name being used at the time.  So if someone named blarg runs `#register password`, they will be registered as blarg.

## Killbox system (mod_killbox.cfg)
The Killbox system creates killboxes around specified areas of the map.  If people are detected in these areas, they are killed automatically.  The script checks everyone in the list every 500 ms.

#### #addkillbox (DESC)
This begins the process of creating a killbox and needs to be run twice.  Adding a description is optional, but recommended for ease of identifying box placement.  Coordinates are grabbed from where the user is standing on the first run.  The user then needs to move to the next spot where the box will end and run the command again, with or without a description.  If a description is entered on the first run, reentering the description is unnecessary unless you want to change it.  Adding a description on the second run will result in the box being created with the second description.

#### #delkillbox [ID]
This command deletes the killbox with the given ID.  IDs can be retrieved by running the `#listkillbox` command.

#### #listkillbox
Returns a list of all killboxes on the current map with the ID, coordinates, and identifying description.