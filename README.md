# Fceux_python_remote_controller
Only tested on fceux2.2.30 and python3.10.4

```
sudo python3
from fceux_python_server import *
waitForConnection()
emu.poweron()


fceux.exe -lua fceux_listener.lua "mario.nes"
```

Original author providid the lua script and "fceux_python_server.py" script and a video:
https://www.youtube.com/watch?v=c3D5gljbkO0

## yingshaoxo guide
### 1. run python listener
```
sudo python3

from python_server import *
waitForConnection()
emu.poweron()
```

### 2. run fceux2.2.30
```
wine fceux.exe

File -> Lua -> New script window -> load 'fceux_listener.lua' script, run it
```


### 3. control the nes game
```
emu.message("hi")
emu.getscreenpixel(0,0,True)

action = { "A" : True, "B":True, "down":False, "right":False, "select":False, "start":True, "up":False }
joypad.write(1, action)
```
