# Torrent-Leecher
A simple web interface for downloading torrent files. Just provide the `magnet` link or `.torrent` file url and sit back. The request is forwaded to a python script that gets the job done. This is very minimalistic implementation of python's `libtorrent` library along with `PHP` and `jQuery`. File browsing is provided by `h5ai` file indexer that has many great features.
##Deploy

[![Deploy of Heroku](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/suryasandy/Torrent-Leecher)
- Home Page
<p align="center"><img src="img/snap_shot.JPG"></p>

- Steps to setup
1. Clone this repository to `/var/www/html/torrent`
2. Make sure `python3.x` is installed. After that, install following packages `sudo apt install python3-libtorrent apache2 php libapache2-mod-php php7.2-gd ffmpeg zip graphicsmagick -y`
3. Edit the file `/etc/apache2/mods-enabled/dir.conf`
4. At the end of line beginning with `DirectoryIndex`, add the line `/torrent/files/_h5ai/public/index.php`
5. Restart the `apache2` server and go to `localhost/torrent`
