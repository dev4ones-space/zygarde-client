# Zygarde
### Zygarde is a open-source _(licenced under GNU General Public License v3.0)_ *remote access tool* made for corporative management, private computer management and many other. _(short description)_
# More about software
### Zygarde is a *remote access tool* _(also known as RAT)_ made specifically for Windows powered machines, and also has a support for other operating systems: macOS (Darwin, High Sierra and higher, limited support), Linux (any distro type, limited support). It's main target and use is to take control over any machine that has installed this software _(malicious use is prohibited)_. To control machine/s you need a control-client, which is present in 2 forms:
- *Telegram*:
  - Pros: fast, easy-to-use
  - Cons: unstable & unproffesional for commercial use _(telegram api may not handle server pretty well)_
- *Terminal Client*:
  - Pros: very fast _(direct connection to server)_, extended support in future, build-in python3 API
  - Cons: hard to use & update for typical user _(requires minimal terminal knowledge)_

## How software works:
### Firstly, when client (basically a RAT itself) is installed & run, it will contact the server (optimized for speed & reliability) for authentication, if server has Telegram supported (turned on in config), first privilleged ID gonna receive a message with button and prompt to authniticate the client and allow to contact server in future for other, and for Terminal Client you will need to check queue by `$ server check-auth-queue` (for servers with manage version of 14 and higher.
### If client was authorized, it will contact server for current task every 10 seconds _(can be changed in code)_ in cycle.
## What client can do:
### Soundpad: play sounds on remote machine, only sounds included in-compiled executeble
### Shell: run shell commands
### Scripts: run build-in scripts which can be added from server or client, build-in ones include: enable RDP, tunnel RDP to relay server (requires SSH no-shell, secure user to be set up), shutdown or reboot and other.
## Technical info:
### Client & server for communication use ZeroRPC, connection and requests are automatically encrypted by TrafficSafe _(to hide & protect data from man-in-middle attack and ISP)_. TrafficSafe is a modem _(.py)_ build-in function to protect traffic from being exposed and has a autheniticaion check _(all non-encrypted traffic will be not processed (discarded))_, also client & server should share same TrafficSafe token
_please notice: documentation and this README is still in progress_
