# Minecraft Server Regulation

This software is meant to regulate minecraft server for automated tasks as reboot with several tasks to be done in a certain order.

It relies on [MSCS](https://github.com/MinecraftServerControl/mscs) for server management and [Skript](https://github.com/SkriptLang/Skript) for command management.


## How it should works

1. Send a command to Skript
2. Wait for command completion
3. Shutdown the servers
4. Backup
5. Update server config
6. Start the servers

Execution relies on a Cron rule.

Errors are handled at any moments. A mail is send with all the information needed (and available).

## Config file

Config is stored into the `config.cfg` file.

|      Key      |          Value         |               Signification              |
|:--------------|:-----------------------|:-----------------------------------------|
| mail-account  | user@domain.com        | The address mail used to send mail alert |
| mail-password | foobar                 | Your mail password                       |
| mail-port     | 465                    | SMTP port                                |
| mail-address  | mail.server.domain.com | Your mail server location                |
| mc-hook       | Lorem ipsum            | How the script will recognize job's done |
| mc-server     | bungeecord             | The server where Skript will echo out    |
