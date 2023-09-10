# Issues

General Github Issues to create for this project. This is a high level list to span project-wide changes,
and will serve as a temporary place where we can agree on things. This should become a simple list of
Github Issues.

### Unit Tests

General updates to improve health of the project. This will make bugs less common, and give others conifidence they
can use this code without issues.

* Pick a testing framework to use (pytest is probably ideal)
* Setup unit tests for this project
* Setup automated tests via github actions
* add 50% code coverage

### Architectual

Architectual changes here are significant changes to how code is internally organized within the project. Moving
code into different classes and such.

* Switch to server-only architecture
    * Clients will not need to install anything to play, and can connect with any dumb telnet/nc client.
* Add CLI for easily starting the service via shell
* Refactor gamemaster.py
    * Create new class to hold all networking code
    * Consider middleware classes to abstract networking send/receive into "turns" for wizard classes
    * Remove low-level logic from gamemaster class, separate into separate objects as needed

### Publication

Publication will allow anyone to easily install and run the game. The goal here is that someone new could do this
to host their own game: 

pip install waving-hands
waving-hands --start

* Expand readme.md with instructions on how to run the game (server, and clients)
    * We may not need instructions for clients if we remove the need for client code
* Add a setup.py
* Add a version file
* Setup automated publication to PYPI