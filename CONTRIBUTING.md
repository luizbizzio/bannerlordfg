# Contributing to BannerlordFG

Build on Windows with Bannerlord installed, Visual Studio 2022 Build Tools or MSBuild, and the .NET Framework 4.7.2 targeting pack. [`BUILD_WINDOWS.cmd`](BUILD_WINDOWS.cmd) shows the configured game path and starts the build. Gameplay and menu code lives in [`src/BannerlordFG`](src/BannerlordFG), and setup and recovery code lives in [`src/BannerlordFG.Setup`](src/BannerlordFG.Setup).

## Review a change

- For graphics changes, verify the in-game Performance menu, the selected upscaler and frame-generation options, and their values after restarting the game.
- Use the relevant harness for setup or diagnostics changes. [`RunDiagnosticsTests.cmd`](tests/RunDiagnosticsTests.cmd), [`RunUninstallSafetyTests.cmd`](tests/RunUninstallSafetyTests.cmd), and [`RunWindowsPolicyTests.cmd`](tests/RunWindowsPolicyTests.cmd) cover different paths.
- For installer or proxy changes, compare install, upgrade, and uninstall using a test game installation. Check that pre-existing graphics files are preserved where expected.

Report the game version, GPU, driver, launcher, and any ReShade or BLSE setup relevant to the result. Review exported diagnostics for identifying paths or device details before attaching them.
