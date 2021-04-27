# torrserver
### Unofficial Docker Image for TorrServer (~30MB)

"TorrServer, stream torrent to http"

More info:
- https://github.com/YouROK/TorrServer
- https://4pda.ru/forum/index.php?showtopic=889960

### Requirements

* docker
* ~200 Mb RAM(caching)

### Installing

- сreate "~/torrserver/db" directory (for example) on your host
```
mkdir -p ~/torrserver/db
docker run -d --name=torrservermatrix --restart=always -v ~/torrserver/db:/torrserver/db -v /etc/localtime:/etc/localtime:ro -p 8090:8090 solopasha/torrserver
```
### Usage
Open ```localhost:8090``` in your browser.
Torrent files, placed in ~/torrserver/db will be added to torrserver automatically.

