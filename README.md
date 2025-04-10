# BepInEx.Harmony

HarmonyXInterop loads all of the 0Harmony.dll's in the BepInEx core files. But, 0Harmony.dll is the only real Harmony file, the rest are all Interops (Generated by the projects like the ones in this repository).
What the interops do is Shim the plugins using old Harmonies to work with HarmonyX. (Shimming makes the plugins use 0Harmony222.dll instead of 0Harmony.dll (version 2.2.2.0))

Just need to reference regular 0Harmony.dll version 2.2.2.0 and the Shim will convert them to use 0Harmony222.dll

**IT DOES NOT LOAD WITH 0Harmony.dll version 2.2.2.0 IT JUST ADAPTS THE PATCH SO THAT IT WORKS WITH 0Harmony.dll version 2.9.0.0 AND ITS NORMALISATION!!**
## Findings

- BepInEx has a warning message for when it is shimming a mod and you can tell if a mod has been shimmed by using dnspy to look into its references.
- HarmonyX22 / HarmonyX2 only marked itself as needing shimming once I added a prefix to it. Transpiler did not.
