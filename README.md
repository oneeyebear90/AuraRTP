Download Aura RTP Plugin from these trusted hosts!

[![Modrinth Version](https://img.shields.io/modrinth/v/aurartp?style=flat-square&logo=modrinth&label=Modrinth)](https://modrinth.com/plugin/aurartp) [![Hangar](https://img.shields.io/badge/Hangar-Aurartp-blue?style=flat-square&logo=paperMC&logoColor=white)](https://hangar.papermc.io/oneeyebear/Aurartp)


# <center>AuraRTP</center>
<br>

**AuraRTP** Not just another Random Teleportation Plugin. AuraRTP helps your players explore the world while protecting your server from lag caused by world generation when using other RTP solutions. AuraRTP targets use on Paper servers and features pre-generated RTP destinations so a player teleporting doesn't have to generate the surrounding world when they teleport, reducing the demand on your server.
<br>

<details>
<summary><b>Optional Integrations</b></summary>

  | <center>Vault</center> | <center>WorldGuard</center> | <center>GriefPrevention</center> |
| :--- | :--- | :--- |

</details>

<p align="center">
  Please report any found bugs on GitHub or Discord!<br><br>
  <a href="https://github.com/oneeyebear90/AuraRTP/issues">
    <img src="https://img.shields.io/github/issues/oneeyebear90/AuraRTP?style=for-the-badge&logo=github" alt="GitHub Issues">
  </a>
  &nbsp;&nbsp;
  <a href="https://discord.gg/XmVXXzZ42u">
    <img src="https://img.shields.io/badge/Discord-Join%20Server-4E9F6E?style=for-the-badge&logo=discord&logoColor=white" alt="Discord">
  </a>
</p>

## 🚀 Why Download AuraRTP?

- **Zero-Lag Instant Teleportation:** Pre-generated coordinate queues stored in SQLite databases ensure players experience instant teleports without server stutter or chunk-loading lag.
- **Optional Teleportation Restrictions:** Configure player cooldowns and command embargoes to prevent players from frequently triggering RTP. Embargoes force players to explore the RTP destination and not just teleport hop. Reducing stress on your server.
- **Optimized for Paper & Async Performance:** Background tasks perform coordinate selection, biome blacklisting, and safety checks asynchronously, with smart idle refills that trigger when when there are no players online.

## <center>🌟 AuraRTP Features</center>

#### _**Customize Teleport Distance and Origin**_

Dimension-specific configuration allows you to specify minimum and maximum teleport distance per world as well as setting a specific Origin location so the minimum and maximum distance is relative to the specified origin location rather than just x 0 z 0 like regular RTP plugins.

#### _**Physical World Triggers**_

Allow players to trigger random teleports simply by right-clicking designated buttons/blocks placed in the world (such as at server spawn).

#### _**Custom World Support**_

Config file allows for adding worlds, enabling/disabling rtp in specific worlds, and supports custom naming if your world doesn't follow the standard Minecraft naming conventions.

#### _**Circular World Border Support**_

Supports both standard and circular world borders.

#### _**Biome Blacklisting**_

Allows for blocking generated coordinates to specific biomes.

#### _**Claim Protection Integration**_

Automatically checks coordinates against popular claim plugins like **WorldGuard** and **GriefPrevention**, ensuring players never teleport inside protected player claims or server regions. 

#### _**Command Embargo & Escape Blocking**_

Prevents players from immediately returning to spawn or home using commands like `/home`, `/spawn`, `/back`, or `/tpa` for a configurable duration after teleporting. While allowing players to still group up at the RTP location using commands like `/tpahere`. Blocked and allowed commands are adjustable in the config.

#### _**Economy & XP Level Costs**_

Optionally charge players Vault economy currency or XP levels to perform random teleports.

---

#### **Note:** 
Command triggered RTP permissions are false by default. You must give permission for players to use commands to trigger RTP.

Custom worlds defined in the config file will require adding the permission using the main world key from the config (not "worldname"). The plugin will add the worlds as valid permissions dynamically after being added to the config. See the section below.

<details open>
<summary><b>📋 Permissions & Commands</b></summary>

| Command / Trigger | Permission | Description | Default State |
| :--- | :--- | :--- | :--- |
| *Physical Trigger (Button)* | `aurartp.rtp.use` | Allows players to right-click configured physical triggers to RTP. | `true` |
| `/aurartp` | `aurartp.rtp.random` | Randomly teleport to any enabled world. | `false` |
| `/aurartp <world>` | `aurartp.rtp.<world>` | Teleport to a specific enabled world from `config.yml` (e.g., `overworld`, `nether`, `end`, or custom world keys). | `false` |
| `/aurartp reload` | `aurartp.admin` | Reload configuration files and coordinate queues. | `op` |
| `/aurartp update` | `aurartp.admin` | Perform an on-demand Modrinth update check. | `op` |
| `/aurartp queue <status\|fill\|clear>` | `aurartp.admin` | Monitor queue sizes, trigger manual fills, or clear world queues. | `op` |
| `/aurartp unembargo <player>` | `aurartp.admin` | Clear an active command embargo for a player. | `op` |

</details>

<details>
<summary><b>⚙️ Current config.yml</b></summary>

[Updated config.yml Reference](https://www.oneeyebear.net/aurartp-config)

</details>
