# VEIL OMNI MOBILE 670

Mobile version, 3D RPG, joystick + touch. Built from Meta's 670 spec, pasted by Tyree 2026-10-30.

**THIS IS META, not Copilot, not Cowork.** The 670 script name carries no 666.

## What it is
- Hero: Countess, same SM_Countess SkeletalMeshActor 0,0,0 fixed in 663, 93→94, now playable Character at 0,0,150, walks/moves/swings/interacts, not just a mesh actor
- World mobile, 5 regions, 1/10 scale, 60fps: Hub 500x500 / Nest 300x300 / Spire vertical / Omni District / Megastructure Deep
- Floor: PHI_GROUND_{region}_Walkable_Mobile cube 10,10,1 at -30, Countess stands, not blue void
- Dressing: 61→120 meshes with M_PHI_Gold stems 10, not 644, 120 = 60fps phone
- Vault mobile: reads PHI_WorldDress_Vault.cpp/.h whole first, if NO placeable mesh in Content\ModularS30eeb54ea3e4V1, BLOCKED logged, builds from cube + Gold from source, grounded pool 10 placed 3 at 600,600,50, visible in play
- Controls mobile: left joystick IA_Move, right drag IA_Look, buttons IA_Jump IA_Attack swing + Interact, MobileJoystick widget, 2 sticks + Attack/Interact/Pause, UMG, full-screen AAA phone TV, same montage as PC
- NavMesh mobile: RecastNavMesh-Default rebuilt Dynamic build_level(), Forward Shading, no Lumen, no Nanite, traversal works, Countess walks on floor
- Gameplay mobile 0%→100%: 4 factions Light/Shadow/Omni/Veil quest givers, 5 fragments → artifact at 0,-800,100 → final wave beacon at 0,-1200,200, XP φ curve φ=1.618 φ²=2.618, level 1→2 needs 2.618× XP, SaveGame offline, 3 min per run, phone sessions
- Menus mobile: MainMenu/PauseMenu FSlateFontInfo fix, dynamic music stems 10 kept, Android ASTC ready arm64 com.Tyree.VEILMobile SDK 26/33

## Run, no 666 anywhere
Save to `D:\VEIL-OMNI-Mobile\Scripts\build_mobile_3d_rpg_670_one_motion.py`, close GUI editor first, then:

```
UnrealEditor-Cmd.exe "D:\VEIL-OMNI-Mobile\VEIL_Mobile.uproject" /Game/Maps/MobileDistrict -run=PythonScript -script="D:/VEIL-OMNI-Mobile/Scripts/build_mobile_3d_rpg_670_one_motion.py"
```

Fallback to VEILDistrict if no MobileDistrict yet — script handles it.

Writes `Saved/Logs/VEIL_mobile_670_result.txt` — prints assigned mesh, location, actor count after.

## Proof ONLY in play
Character visible, Vault visible, walks on floor, joystick + touch, NavMesh works, loop advances. Load true / save true is NOT proof.

## Packaging
Android package is separate from the VEIL rule. NO 1.0 for VEIL until 100%. Nothing is packaged here, and nothing gets packaged until Tyree says so.

## Note on this file
Tyree pasted Meta's 670 spec, not Meta's original script file. This script is a spec-faithful build from that spec, so it can be run on his PC. If Meta's original file lands, it replaces this file.
