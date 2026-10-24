# Project PHOENIX v0.1 — Starter scaffold

A Fabric client-side project targeting Minecraft Java Edition **1.21.11**.
The long-term goal is to investigate measurable performance improvements for
low-end Android devices running Minecraft through compatible Java launchers.

## Important status

This is a **starter scaffold**, not an FPS-boosting release. It currently
registers a basic Fabric mod entry point and writes startup messages to the
Minecraft log. It does not modify rendering, memory management, or gameplay.
Do not advertise it as an FPS booster until optimizations have been implemented
and measured on real devices.

## Initial target

- Minecraft: 1.21.11
- Java: 21
- Fabric Loader: 0.18.4
- Fabric API: 0.141.1+1.21.11
- Fabric Loom: 1.14-SNAPSHOT

If Fabric's version recommendations change, update these values together.

## Build without installing tools on your phone

This repository includes a GitHub Actions workflow. After uploading these
files to a GitHub repository:

1. Open the repository on GitHub.
2. Open **Actions**.
3. Select **Build Project PHOENIX**.
4. Press **Run workflow** if the workflow has not started automatically.
5. Open the completed run and download the `phoenixmobile-dev-jar` artifact.
6. Test only in a separate Minecraft profile, after backing up worlds.

The workflow uses GitHub-hosted build runners. GitHub account usage limits
and availability may apply.

## Install for testing

Copy the built `phoenixmobile-0.1.0.jar` into the `mods` folder of a separate
Minecraft 1.21.11 Fabric profile that has Fabric API installed. The launcher
must support that Minecraft version and Fabric Loader. A successful build
does not guarantee compatibility with every Android launcher or renderer.

## Development roadmap

1. Build and launch this baseline.
2. Record a repeatable baseline: FPS/frame times, RAM, chunk loading, and
   stutters in the same world and settings.
3. Profile CPU and rendering bottlenecks before changing code.
4. Implement one small, reversible optimization at a time.
5. Compare results against the baseline and test crashes, visuals, and
   compatibility before publishing.

## License

MIT
