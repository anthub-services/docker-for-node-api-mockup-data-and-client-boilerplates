# Docker for Node API Mockup Data and Client Boilerplates

This project is based on the
[Node API and Client Boilerplate](https://github.com/anthub-services/node-api-and-client-boilerplate).
With [Docker](https://www.docker.com/), you can start all the services
([Node Express API Mockup Data Boilerplate](https://github.com/anthub-services/node-express-api-mockup-data-boilerplate) and
[Create React App Boilerplate](https://github.com/anthub-services/create-react-app-boilerplate) with one bash command.

## Other Docker Boilerplates

- [Docker for Node API and Client Boilerplates](https://github.com/anthub-services/docker-for-node-api-and-client-boilerplates)
- [Docker for Rails API and Client Boilerplates](https://github.com/anthub-services/docker-for-rails-api-and-client-boilerplates)

## Docker

Download and install the [Docker Community Edition](https://www.docker.com/community-edition).

## Bash Commands

Executable bash commands have been provided to easily execute Docker commands.
From the `root` directory of the project, run the following commands:

| Command                              | Description                                                                   |
|--------------------------------------|-------------------------------------------------------------------------------|
| `bin/install`                        | Clone the apps, build the Docker containers, and start the apps               |
| `bin/reinstall`                      | Delete then clone the apps, rebuild the Docker containers, and start the apps |
| `bin/start`                          | Start all the services (API and client)                                       |
| `bin/stop`                           | Stop all the services                                                         |
| `bin/console <container ID or Name>` | Access the terminal console of the API or client containers                   |

Note: To manage separate Docker instance for API or client,
open another terminal console and change the project directory from `root` to `api` or `client` and run the commands above.

### CSS

| Command         | Description                                                         |
|-----------------|---------------------------------------------------------------------|
| `bin/css/watch` | Watch and compile *.scss files on file changes (for Mac users only) |
| `bin/css/build` | Manually compile *.scss files                                       |

Note: To run the commands above for separate client Docker instance, simply change the project directory from `root` to `client`.

## Install and Start the Apps
Run the `bin/install` to clone the API and client apps.
If the installation process is successful, both the API and client services shall be started.

## Users

Use the following credentials to test different API responses. Default password for all accounts is `password`.

| Name              | Email                  | Description |
|-------------------|------------------------|-------------|
| Super Admin User  | `superadmin@email.com` | Has wildcard access |
| Admin User        | `admin@email.com`      | Has wildcard access but `Admin › Users › Delete` is excluded |
| Common User       | `user@email.com`       | Can access `My Profile`, `Admin › Dashboard`, `Users`, `Users › View, and Settings` |
| Referrer User     | `referrer@email.com`   | When `redirect` is set without the domain, e.i. `/admin/dashboard`, user shall be redirected to internal page if no location path (referrer) found on the Sign In page |
| Redirect User     | `redirect@email.com`   | When `redirect` is set with complete URL, e.i. `https://github.com/anthub-services`, user shall be redirected to external page if no location path (referrer) found on the Sign In page |
| Blocked User      | `blocked@email.com`    | User is signed in but the account is blocked |
| Unauthorized User | `<any invalid email>`  | Simply enter wrong `email` and/or `password` |
