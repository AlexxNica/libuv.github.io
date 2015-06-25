# The libuv website

This branch contains the source files for the libuv website.


## Building

In order to build the website you need to have Node/iojs, bower and gulp
installed. Assuming you already have `npm` on your path, run:

    npm install -g bower gulp

Once those are installed, install the project dependencies:

    npm install
    bower install

Run the test webserver:

    gulp serve

Create the distributable website:

    gulp build


## Deploying

Right now this is a bit manual. It will be improved in the future with a gulp
task.

    # Make sure you are on the 'src' branch and you comitted all changes
    # Build the website
    gulp build
    # Change the branch to master
    git checkout master
    # Copy the generated files over
    cp -r dist/* .
    # Commit the result
    git commit -a -m "Update"
    # Push!
    git push --all

