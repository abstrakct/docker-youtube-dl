# youtube-dl
Automatically backup YouTube Channels

forked from timlinden

Optional environment variable 'DOWNLOAD_RATE' will set maximum download rate. See youtube-dl manpage for details.

Example docker-compose entry:

`
youtube-dl:
  image: vortexsurfer/youtube-dl
  container_name: youtube-dl
  environment:
    - DOWNLOAD_RATE=500K
  volumes:
    - /path/to/download/directory:/downloads
  restart: unless-stopped
`

Videos will be downloaded to the /downloads directory. Put all the channels you want to automatically download in a file named channels.txt in the /downloads directory. See youtube-dl manpage for details.
