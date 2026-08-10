# Custom Modpack Changelog & Modifications Log

This document tracks all custom mods added, updated, and patched in this instance of **All the Mods 9 (ATM9)**.

---

## 1. 🛠️ Binary Mod Patches (Custom Compatibility Fixes)

The following mods contained mixin or class signature conflicts with updated core dependencies and were patched locally:

### 1. `appliedsoul-1.20.1-1.0.0.jar`
- **Issue:** Crashed on launch due to `industrialforegoingsouls` refactoring mixin methods.
- **Patch Applied:** Modified `appliedsoul.mixins.json` to set `"defaultRequire": 0`.

### 2. `applied_greg-1.0.3.jar`
- **Issue:** Crashed on launch with GregTech CEu 7.5.3 due to signature changes.
- **Patch Applied:** Modified `mixins.applied_greg.json` to set `"defaultRequire": 0`.

### 3. `extendedae_plus-1.5.5.jar`
- **Issue:** Mixin collision in `AdvPatternProviderLogicAdvancedMixin.class` when running alongside `AdvancedAE`.
- **Patch Applied:** Recompiled `AdvPatternProviderLogicAdvancedMixin.class` with non-conflicting method signatures and updated jar bytecode. Source code is tracked at `src/com/extendedae_plus/mixin/advancedae/helpers/AdvPatternProviderLogicAdvancedMixin.java`.

---

## 2. ➕ Manually Added Mods & Addons

### ProjectE & Transmutation Suite
- `ProjectE-1.20.1-PE1.0.1.jar`
- `autoemc-2.0.1.jar`
- `ProjectE_Integration-1.20.1-7.2.5.jar`
- `projectexpansion-1.20.1-1.1.3.jar`
- `teamprojecte-1.20.1-1.1.4.jar`
- `TeamProjectExpansion-1.20.1-1.2.0.jar`
- `emc-interface-1.20.1.1.jar`
- `forbidden_arcanus_emc-0.1.0+forge-1.20.1.jar`
- `irons_spellbooks_emc-0.1.0+forge-1.20.1.jar`

### Applied Energistics 2 (AE2) Addons
- `extendedae_plus-1.5.5.jar`
- `AppliedVoltex-1.0.2.jar`
- `appliedsoul-1.20.1-1.0.0.jar`
- `applied_greg-1.0.3.jar`
- `assembler-matrix-prioritization-forge-1.20.1-1.0.3.jar`
- `crazyae2addons-3.2.3-all.jar`
- `rechiseledae-1.0.1-forge-mc1.20.1.jar`
- `appliedcooking-4.0.0.jar`
- `appliedcreate-1.20.1-1.1.6.jar`
- `appliedenoughitems-1.1.1.jar`
- `appliedpneumatics-1.20.1-forge-1.0.8.jar`
- `appliedsorting-1.20.1-forge-v2.0.0.jar`

### Logistics & Mechanics
- `logisticspipes-0.0.2.jar`
- `Re-Avaritia-forge-1.20.1-1.4.1-release.jar`
- `AvaritiaTweak-forge-1.20.1-1.3.0-release.jar`
- `avaritia_delight-0.3.4.jar`
- `mekanism_avaritia-0.1.jar`
- `Evolved Mekanism-1.20.1-1.2.1-fix4.jar`

---

## 3. ⬆️ Updated Core Mods

- **Forge Loader:** `47.4.0` ➔ `47.4.22`
- **Applied Energistics 2:** `15.4.9` ➔ `15.4.10`
- **AE2 Wireless Terminal Library (ae2wtlib):** `15.3.0` ➔ `15.3.3`
- **AppBot:** `1.5.1` ➔ `1.5.2`
- **GregTech CEu:** `7.2.0` ➔ `7.5.3`
- **Blood Magic:** `3.3.3-45` ➔ `3.3.8-50`
- **Industrial Foregoing:** `3.5.21` ➔ `3.5.22`
- **Fusion:** `1.2.11+a` ➔ `1.3.12`
- **Rechiseled:** `1.1.6` ➔ `1.2.5`
- **Rechiseled Create:** `1.0.2+b` ➔ `1.1.1`
- **SuperMartijn642 Core Lib:** `1.1.18` ➔ `1.1.23+a`
- **Balm:** `7.3.37` ➔ `7.3.42`

---

## 4. ⚙️ Configuration & KubeJS Fixes

- **`config/autoemc-common.toml`**: Configured `#croptopia:seeds=16` and `#croptopia:crops=32` baseline EMC values; enabled `alwaysRescan = true`.
- **`defaultconfigs/ftbessentials-server.snbt`**: Enabled `/fly` and `/back` (max history 10).
- **`kubejs/server_scripts/tags.js`**: Added missing `#productivebees:flowers/lepidolite` tag definition for GTCEu apiary compatibility.
