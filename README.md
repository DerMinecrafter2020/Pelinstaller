# Pelinstaller

[![License: GPL v3](https://img.shields.io/github/license/Zinidia/Pelinstaller)](LICENSE.md)

## Verwendung der Installationsskripte

Um die Installationsskripte zu verwenden, führen Sie einfach diesen Befehl als Root aus. Das Skript fragt Sie, ob Sie nur das Panel, nur Wings oder beides installieren möchten.

```bash
bash <(curl -Ss https://raw.githubusercontent.com/DerMinecrafter2020/Pelinstaller/refs/heads/Production/install.sh || wget -O-https://raw.githubusercontent.com/DerMinecrafter2020/Pelinstaller/refs/heads/Production/install.sh) auto
```

_Notiz: Auf einigen Systemen muss man bereits als root angemeldet sein, bevor man den einzeiligen Befehl ausführt (wobei `sudo` vor dem Befehl nicht funktioniert).._

⚠️ Warnung: Derzeit gibt es ein Problem, bei dem Pelican Dateien erstellt, die dem falschen Linux-Benutzer gehören, wenn bestimmte Funktionen im Admin-Panel aktiviert sind. Um dieses Problem zu beheben, müssen Sie möglicherweise die Berechtigungen anpassen, indem Sie den folgenden Befehl ausführen: `chown -R www-data:www-data /var/www/pelican`. Weitere Informationen finden Sie in der Dokumentation von Pelican. [troubleshooting guide](https://pelican.dev/docs/troubleshooting/).

## Funktionen

- Automatische Installation des Pelican Panels (Abhängigkeiten, Datenbank, Cronjob, Nginx).
- Automatische Installation der Pelican Wings (Docker, systemd).
- Panel: (optional) automatische Konfiguration von Let's Encrypt.
- Panel: (optional) automatische Konfiguration der Firewall.
- Unterstützung bei der Deinstallation sowohl des Panels als auch der Wings.

## Unterstützte Versionen 

Liste der unterstützten Installationskonfigurationen für Panel und Wings (Installationen, die von diesem Installationsskript unterstützt werden).

### Unterstützte Panel und Wings Version

| Operation System | Version | Unterstützt        | PHP Version |
| ---------------- | ------- | ------------------ | ----------- |
| Ubuntu           | 16.04   | :red_circle:       |             |
|                  | 18.04   | :red_circle: \*    |             |
|                  | 20.04   | :white_check_mark: | 8.3         |
|                  | 22.04   | :white_check_mark: | 8.3         |
|                  | 24.04   | :white_check_mark: | 8.3         |
| Debian           | 8       | :red_circle: \*    |             |
|                  | 9       | :red_circle: \*    |             |
|                  | 10      | :white_check_mark: | 8.3         |
|                  | 11      | :white_check_mark: | 8.3         |
|                  | 12      | :white_check_mark: | 8.3         |
|                  | 13      | :white_check_mark: | 8.3         |
| CentOS           | 6       | :red_circle:       |             |
|                  | 7       | :red_circle: \*    |             |
|                  | 8       | :red_circle: \*    |             |
| Rocky Linux      | 8       | :white_check_mark: | 8.3         |
|                  | 9       | :white_check_mark: | 8.3         |
| AlmaLinux        | 8       | :white_check_mark: | 8.3         |
|                  | 9       | :white_check_mark: | 8.3         |

_\* Bezeichnet ein Betriebssystem und eine Version, die zuvor von diesem Skript unterstützt wurden._

## Firewall Einrichtung

Die Installationsskripte können eine Firewall für Sie installieren und konfigurieren. Das Skript fragt Sie, ob Sie dies wünschen oder nicht. Es wird dringend empfohlen, sich für die automatische Firewall-Einrichtung zu entscheiden.

## Ersteller ✨

Wir möchten uns bei den folgenden Mitwirkenden für ihre Arbeit bei der Pflege und Erstellung dieses Installationsprogramms bedanken:
1) [Matthew Jacob](https://github.com/Zinidia)
2) [Vilhelm Prytz](https://github.com/vilhelmprytz)
3) [Linux123123](https://github.com/Linux123123)
4) [ImGreen](https://github.com/GreenDiscord)
5) [Neon](https://github.com/DeveloperNeon)
6) [sam1370](https://github.com/sam1370)
7) [Linux123123](https://github.com/Linux123123)
8) [sinjs](https://github.com/sinjs)

Copyright (C) 2018 - 2024, Vilhelm Prytz
Copyright (C) 2021 - 2024, Matthew Jacob
