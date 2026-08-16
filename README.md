PROJECT ERIS ++ 1.0.21 - SETUP GUIDE
=====================================

OVERVIEW
--------
Project Eris ++ upgrades an existing Project Eris USB installation with the proven Project Eris ++ runtime, local Achievement Hub, controller/rumble integration, save-state resume/preview bridge and genuine RetroAchievements-based achievement packs.

This release uses one simple Windows front end. After Project Eris ++ is installed to the USB, the app offers three game choices only:
- Install One Game
- Install a Game Folder
- Use Current USB Library

REQUIREMENTS
------------
- Windows 10 or Windows 11, 64-bit.
- A working Project Eris USB drive for the PlayStation Classic.
- Enough free USB space for the existing first-boot Internal 20 export preflight.
- Your own legally obtained PlayStation game images and BIOS files where required.

Project Eris ++ does NOT include PlayStation BIOS files, ROMs/disc images, RetroAchievements credentials, DuckStation or RA_Integration.dll.

WINDOWS INSTALLATION
--------------------
1. Run Project_Eris_PlusPlus_Setup_v1.0.21.exe.
2. Accept the per-user Windows installation. Administrator rights are not normally required.
3. Start Project Eris ++ from the Desktop or Start Menu shortcut.
4. Insert the Project Eris USB drive.
5. Wait for the USB check to pass.
6. Enter a profile name if you want to change the default.
7. Click INSTALL PROJECT ERIS ++ TO USB.
8. The existing Project Eris ++ deployment code creates a backup before changing the USB.
9. When installation completes, choose one of the three game workflows.

OPTION 1 - INSTALL ONE GAME
---------------------------
Choose one supported launch image: M3U, CUE, PBP, CHD or ISO. The existing FDB-first workflow prepares genuine achievement data before accepted content is copied to the Project Eris transfer folder. CUE dependencies are kept together.

OPTION 2 - INSTALL A GAME FOLDER
--------------------------------
Choose a folder containing your PlayStation game library. The folder is scanned recursively. Existing M3U files have priority, CUE dependencies are preserved, and supported multi-disc naming can be grouped automatically. Accepted games use the same FDB-first transfer workflow.

OPTION 3 - USE CURRENT USB LIBRARY
----------------------------------
Use this when games are already installed on the Project Eris USB. Project Eris ++ scans the normal Project Eris games locations, reads Game.ini titles when available and recognizes M3U/CUE/PBP/CHD/ISO layouts. Existing game images are NOT copied, moved or renamed. Only Project Eris ++ achievement metadata, aliases and UI data are updated.

DUCKSTATION AND RAINTEGRATION
-----------------------------
DuckStation is only required when Project Eris ++ cannot find a validated local achievement cache/FDB for a game. Install DuckStation normally and place RA_Integration.dll next to the DuckStation executable. Enable RAIntegration and sign in to RetroAchievements. Project Eris ++ intentionally does not bundle or download these third-party files.

TROUBLESHOOTING
---------------
- If the USB is not detected, confirm Project Eris itself boots and that its normal configuration exists on the USB.
- If preflight fails, the installer does not change the USB. Read the status message and correct the missing Project Eris file or free-space problem.
- If a game is blocked, verify DuckStation can start that game, RA_Integration.dll is next to DuckStation, RAIntegration is enabled, and the RetroAchievements cache is available.
- Reports are written to the USB after game operations.
- For runtime diagnostics, use Check_Runtime_After_Test.bat after a PlayStation Classic test.

BUG FIX
-------
The legacy Manager performance-mode event now uses its event sender instead of the outer $modeBox variable. This prevents the uninitialized-variable JIT exception reported in 1.0.20.

THIRD-PARTY NOTICE
------------------
Project Eris ++ is an unofficial community add-on and is not affiliated with Sony, ModMyClassic/Project Eris, Libretro/RetroArch, DuckStation or RetroAchievements.

Copyright Frozsti 2026.
