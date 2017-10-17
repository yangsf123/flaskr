
study flask framework from http://flask.pocoo.org/docs/0.12/tutorial/folders/#tutorial-folders

step0: create the applications directory structure.
    mkdir flaskr && cd flaskr
    mkdir flaskr && cd flaskr
    mkdir static    # available to users of the application via HTTP.This is the place where CSS and JavaScript files go.
    mkdir templates

step1: create the database schema.
    # Only a single table is needed for this application and it will support SQLite.
    # put the following contents into a file named schema.sql in the flaskr/flaskr folder:
    drop table if exists entries;
    create table entries (
            id integer primary key autoincrement,
            title text not null,
            'text' text not null
    );

step2: application setup code
    # Now that the schema is in place, you can create the application module,flaskr.py
    # This file should be placed inside of the flaskr/flaskr folder.The first several lines of
    # code in the application module are the needed import statements. After that there will ba a few
    # lines of configuration code. It is possible to drop the configuration directory into the module.
    # We can create a separate .ini or .py file,load that,and import the values from there.

    tips: http://flask.pocoo.org/docs/0.12/config/#instance-folders


step3: installing flaskr as a package
        tips: command line address http://click.pocoo.org/5/


step4: database connections
    # Flask provides two contexts: the application context(g) and the request context(request).
    # use the application context can manager the database connection.


step5: creating the database
