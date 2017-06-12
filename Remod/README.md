# Remod Script Descriptions

## User system (mod_login.cfg)
This is a basic user system for name-protection.  It can use either the default SQLite database or a MySQL database.  A table is created on first-run to store the user information.  The script currently features two commands: #login, #register.

#### #login [USERNAME] [PASSWORD]
This will log a user in if the information provided is correct.  Users are able to login to their registered name under an alias assuming the alias being used is not protected.  When a logged in user disconnects, they will be logged out.  If a user connects under a protected name, they are muted and will remain muted until they login or change to an unprotected name.

#### #register [PASSWORD]
This command registers a user using the name being used at the time.  So if someone named blarg runs `#register password`, they will be registered as blarg.
