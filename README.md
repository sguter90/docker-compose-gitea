# Docker-Compose-Gitea

A Docker Compose file for Gitea - Git with a cup of tea ([gitea.io](https://gitea.io))

Data will be saved in separate docker volumes to enable easy upgrades!

## Getting Started

1. Copy .env.dist to .env and make your modifications
2. Start docker containers:
```
$ docker-compose up -d
```

After that open gitea installer via Browser: [http://localhost:3000](http://localhost:3000) and fill the form according your .env settings. 

Set `gitea-db:3306` in _Host_ field and complete setup.

After setup is complete register a new user (use link from the navigation bar).

The first registered user has admin privileges.


### Requirements

* docker
* docker-compose


### Configuration

| VARIABLE              | Description                       | DEFAULT       |
| ----------------------|-----------------------------------|:-------------:|               
|GITEA_VERSION          | Docker-Image-Version              |latest         |
|GITEA_HOSTNAME         | Hostname for Gitea Application    |localhost      |
|GITEA_WEB_PORT         | GUI-Port for accessing Gitea      |3000           |
|GITEA_SSH_PORT         | Port for accessing Gitea via SSH  |2222           |
|MYSQL_ROOT_PASSWORD    | MySQL root password               |root           |
|MYSQL_DATABASE         | Database name for gitea           |gitea          |
|MYSQL_USER             | Database user for gitea           |gitea          |
|MYSQL_PASSWORD         | Password for MySQL user           |gitea          |
