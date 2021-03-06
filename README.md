# My Message in a Bottle

This is the main repository of microservice-based My Message in a Bottle application, project of **Advanced Software Engineering** course of the MSc in Computer Science, University of Pisa.

#### Members

Mark with *bold* the person(s) that has developed this microservice.

|Name and Surname    | Email                         |
|--------------------|-------------------------------|
|*Laura Norato*      |l.norato@studenti.unipi.it     |
|*Emanuele Albertosi*|20783727@studenti.unipi.it     |
|*Michele Zoncheddu* |m.zoncheddu@studenti.unipi.it  |
|*Alessio Russo*     |a.russo65@studenti.unipi.it    |
|*Matteo Pinna*      |m.pinna10@studenti.unipi.it    |


## Overview
The project is an implementation of the [monolith](https://github.com/NennoMP/my-message-in-a-bottle) application with a microservice-based architecture, specifically splitting the previous monolith in at least three microservices. In short, users can register to the platform, customize their profile section, report/block/unblock other users with negative behaviour, exchange time-capsule messages (implemented with **Celery** tasks running in the background) etc..

## Instructions

### Clone the repository

To clone the repository you have to specify the recursive parameter,
in this way:

`git clone --recursive git@github.com:<team_leader_username>/<main-project>.git`

All the submodules will be fetched from GitHub and they will be
placed inside the project root.

### Add a submodule

If you want to add a microservice (hence a submodule), you
have to run the command:

`git submodule add -b <branchName> <repoURL>`

### Pull the updates from all repositories

If a developer has pushed to <branchName> branch and you want
to pull the updates, you have to run the following command:

`git submodule update --remote`

#### Documentation

If you are not familiar with git submodules or you have some
doubts about it, you can check the git-scm documentation
[here](https://git-scm.com/book/en/v2/Git-Tools-Submodules). 

## Configuration

Each micro-service should have a single configuration file, placed inside the main project root, with the name `<microservice_name>_ms.conf`. An example of this can be found in the project root.

## Development

The project structure should be the following:

## Build and run

Application is built with docker-compose. To build the environment
you have to run

`docker-compose build`

To startup application you can issue the following command:

`docker-compose run`

#### Application Environment

The default application environment for this application is **production**.