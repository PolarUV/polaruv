README: Eng, [Rus](README.ru.md)

# PolarUV platform

```mermaid
flowchart TB
    subgraph Polaruv Server
        Settings["`Settings subsystem`"]
        Control["`Control subsystem`"]
        Video["`Video subsystem`"]
        
    end

    UDP["`Native udp protocol`"]
    RTP["`UDP multicast RTP`"]
    Web["`Classic web application`"]

    Settings --> UDP
    Settings --> Web
    Control --> UDP
    Video --> RTP
```

```mermaid
flowchart TB
    Robot["Polaruv server"]
    subgraph Controllable
        Client["`Windows client`"]
        Android["`Android client`"]
    end

    subgraph Settings
        Web["`Web client`"]
    end

    Robot <-- UDP Settings --> Client
    Robot <-- Video --> Client
    Robot <-- Control --> Client
    Robot <-- WEB Settings --> Android
    Robot <-- Control --> Android
    Robot <-- Video --> Android
    Robot <-- WEB Settings --> Web
```

[Releases](https://github.com/PolarUV/polaruv/releases)

[Issues](https://github.com/PolarUV/polaruv/issues)

# PoalrUV clinet

[Installation guide](https://github.com/PolarUV/polaruv/wiki/Client) (wip)

# PolarUV robot

[Intallation guide](https://github.com/PolarUV/polaruv/wiki/Robot) (wip)
