# AdminCore 3.0.0 — Source Release

AdminCore is a Paper plugin source project with one 27-slot administration GUI and a subtle animated space-colour border.

## Included
- `/admincore` (aliases `/acore`, `/admin`) opens the single AdminCore GUI.
- `/help`, `/help 1`, `/help 2`, `/help vanish`, and `/ahelp`.
- GUI controls: vanish, flight, god mode, freeze nearest player, teleport to nearest player, inspect nearest player's inventory, set day, and toggle join lockdown.
- Permission checks, vanish/lockdown bypass, GUI click protection, animation task cleanup, and player-state cleanup on quit/disable.
- Space animation cycles through dark, blue, purple, and cyan glass on decorative slots every 3 ticks by default. Action buttons are not overwritten.

## Build requirements
- JDK 25
- Gradle 8.14+ (or a compatible newer Gradle)
- Paper API `26.1.2-R0.1-SNAPSHOT` repository availability

Build with:
```bash
gradle clean build
```
The plugin JAR will be in `build/libs/`.

## Install
Copy `build/libs/AdminCore-3.0.0.jar` into the server's `plugins/` folder and restart the server.

## Important compatibility note
This ZIP contains source code, not a compiled JAR. The Paper API snapshot for `26.1.2` must be published and reachable when Gradle resolves dependencies. The project has not been compiled against a live server in this environment; build and test it on a staging server before production use.

## Permissions
- `admincore.use` — open GUI (default op)
- `admincore.help` — read help (default true)
- `admincore.vanish`, `admincore.fly`, `admincore.god`, `admincore.freeze`
- `admincore.teleport`, `admincore.inventory`, `admincore.time`, `admincore.lockdown`
- `admincore.bypass` — bypass vanish visibility and lockdown
