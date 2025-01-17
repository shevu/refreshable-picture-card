# Refreshable Picture card #


<img src="https://github.com/dimagoltsman/refreshable-picture-card/raw/master/example1.png" height="400">

<img src="https://github.com/dimagoltsman/refreshable-picture-card/raw/master/example2.png" height="400">

```
resources:
  - url: /hacsfiles/refreshable-picture-card/refreshable-picture-card.js
    type: module
```


configuration is very easy. you can set a picture from a URL or a picture from an entity attribute

attribute picture example:

```
type: 'custom:refreshable-picture-card'
title: My Mibox
update_interval: 3 # default is 30
entity_picture: media_player.livingroom_mibox
attribute: entity_picture

```

url image example:
```
type: 'custom:refreshable-picture-card'
title: My Mibox
update_interval: 3 # default is 30
static_picture: /api/media_player_proxy/media_player.livingroom_mibox?token=11111111111111222222222233333333&cache=1589898123.724253

```

reolink camera snap url example:

```
type: 'custom:refreshable-picture-card'
title: Reolink Camera
update_interval: 1
static_picture: http://192.168.1.174/cgi-bin/api.cgi?cmd=Snap&channel=0&rs=someString&user=username&password=password

```

tap action example: 

```
type: 'custom:refreshable-picture-card'
title: Reolink Camera
update_interval: 1
static_picture: http://192.168.1.174/cgi-bin/api.cgi?cmd=Snap&channel=0&rs=someString&user=username&password=password
tap_action:
  call: remote.send_command
  data:
    entity_id: remote.living_room_remote
    command: b64:JgCgAJSSEg8QEBIPERAPMhEyDxERDxAxEDESLxAyEREPEREQEBAQlBARDxIQEBAREi8PMhEvEhAQMRExDzIREBARDhISDhAyEBEQEQ8REi8RAAdclJMRDxAREREPEREwEi8SEBARDzIQMhAwDzESEBARERAQEBKSEg8QEBAREREPMREyDjESDhIwETESLxEQEBEREBAQETAPERERERAQMRAADQUAAAAAAAAAAA==

```

no margin (full card picture) example:

```
type: 'custom:refreshable-picture-card'
static_picture: http://192.168.1.174/weatherForecast/weather.jpg
noMargin: true

```

navigate example (onclick, open url in new tab): 

```
type: 'custom:refreshable-picture-card'
title: Reolink Camera
update_interval: 1
static_picture: http://192.168.1.174/cgi-bin/api.cgi?cmd=Snap&channel=0&rs=someString&user=username&password=password
navigate: https://github.com/dimagoltsman/refreshable-picture-card/
```



# you are also welcome to contribute #



