# Delta Phi Website
By Jeremiah Nofrada, Vincent Xu, and Jason Yao

## Description
This repo contains all code, documentation, and installation instructions
in order to run the chapter website for the Delta Phi chapter of Phi Kappa Sigma
at New York University.

## What's in this repo
This repo is split off into different sections for ease of maintenance
and installation.

### [Docs](docs/)
This section contains all project design documentation, along with
brainstorming sessions and any other architectural decisions.

### [Letsencrypt](letsencrypt/)
An automated way to request and install TLS certificates.

### [Nginx](nginx/)
An extremely fast and robust reverse proxy server used to serve static content,
all other requests are sent upstream if a cached version is not available.

### [uWSGI](uwsgi/)
The python web server that is the entrance to the application layer of the [website](website/) service being run.

### [Website](website/)
The server actively serves the application content from here.

## Maintenance
General maintenance should be simplified to the point
where a non-technical brother may maintain the full site
from the administration backend at [skullhouse.nyc/admin/](https://www.skullhouse.nyc/admin/).

## Initial Setup (Just use the install scripts in each folder)
1.) Secure fresh VPS with [personal dotfiles](https://www.github.com/JasonYao/dotfiles)

2.) Install nginx + link nginx files

3.) Install Letsencrypt

4.) Install pyenv + pyenv-virtualenv + Python 3.6.0

5.) Install uWSGI

6.) Install Django + point to application files

7.) Install pSQL

## Goals
- Provide information to potential new members
- Provide member services for current members
	- Automatic Bobst study room bookings
	- Public & Private scheduling
	- Automatic chapter minutes emailer
	- VPN services (US & China-specific)
	- Official officer email addresses
- Mobile-optimised

## Technology Stack
Overarching tech design:
- Single provisioned server

Single Tech Stack Design (metal up):
```
[Operating System]:       Ubuntu 16.04 x86_64
[Load Balancer]:          nginx
[Application Server]:     uWSGI + nginx
[Application Framework]:  Django
[Relational Database]:    pSQL
```

## License
This repo is licensed under the terms of the GNU GPL v3 license,
a copy of which may be found [here](LICENSE).
