# 🧾 Case #002 - ROM Analysis and Firmware Patch Attempt

**Drive Model:** Western Digital WD5000LUCT-63C26Y0  
**Capacity:** 500GB  
**Interface:** SATA  
**Date Diagnosed:** 13/09/2023

---

## 🛠️ Symptoms

- Drive spinning but not recognized by BIOS or data recovery software.
- No unusual clicking, but failed to initialize firmware properly.

---

## 🔬 Diagnostic Steps

1. Standard read attempts via recovery tools failed.
2. Firmware-level corruption was suspected.
3. ROM dump was performed using a TTL adapter and WD-specific utility.
4. SYS modules were manually edited using a hex editor.
5. Firmware lock bypassed, allowing full drive initialization.

---

## 🎥 Evidence

- [Watch video of ROM analysis and patch process](../evidences/case_002/case_002_rom_analysis.mp4)

---

## 🧪 Analysis

The firmware on this WD drive was found to be corrupted in specific SYS modules that control initialization routines. After dumping the ROM, certain firmware zones were patched and re-uploaded, successfully bypassing the firmware lock.

The process required low-level access through vendor tools and precise editing of checksum-protected firmware segments.

---

## ✅ Outcome

**Status:** Fully Recovered  
**Reason:** Firmware corruption successfully bypassed by modifying ROM and SYS files.

---

## 🧠 Notes

- This case demonstrates successful firmware-level intervention on a WD 2.5” SATA drive.
- Tools used: WDMarvel (or similar), TTL adapter, Hex Editor, PC-3000 (for validation).

[⬅ Back to Case Index](../README.md) • [📁 View Evidence Folder](../evidences/case_002/)
