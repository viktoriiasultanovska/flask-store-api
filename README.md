## Initialize the database with Flask-Migrate
Activate your virtual environment and run this command:

```flask db init```

This will create a migrations folder inside your project folder.

In the migrations folder, you'll find a few things:

The versions folder is where migration scripts will be placed. Alembic will use these to make changes to the
database.
```alembic.ini``` is the Alembic configuration file.
```env.py``` is a script used by Alembic to generate migration files.
script.py.mako is the template file for migration files.
Generate the first migration to set up the database
Now that we're set up, we need to make sure that the database we want to use is currently empty. In our case, since
we're using SQLite, delete data.db.

Then, run this command:

```flask db migrate```

This will create the migration file.

Now let's actually apply the migration:

```flask db upgrade```

This will create the ```data.db``` file. If you were using another RDBMS (like PostgreSQL or MySQL), this command would
create
the tables using the existing model definitions.

https://rest-api-flask-store-rx6p.onrender.com