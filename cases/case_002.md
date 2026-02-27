# Case 002 – ROM Extraction & Firmware Integrity Analysis

---

## 1. Abstract

500GB WD 2.5” SATA HDD presented with spin-up behavior but failed to initialize at host level.  
Initial diagnostics indicated firmware-level initialization failure.  

A controlled ROM extraction and structured firmware integrity analysis was performed.  
Post-validation, corrected firmware parameters allowed full drive initialization and successful logical data access.

---

## 2. Device Information

- **Model:** Western Digital WD5000LUCT-63C26Y0  
- **Capacity:** 500GB  
- **Interface:** SATA  
- **Form Factor:** 2.5”  
- **Case Date:** 13/09/2023  

---

## 3. Reported Symptoms

- Drive spins normally.
- No abnormal mechanical noise.
- Not detected by BIOS.
- Fails to complete firmware initialization sequence.
- No stable Identify response.

---

## 4. Initial Diagnostics

### 4.1 Mechanical Evaluation
- No audible head recalibration anomalies.
- No signs of mechanical instability.

### 4.2 Logical / Firmware Indicators
- Standard read attempts unsuccessful.
- Behavior consistent with firmware integrity failure.
- Corrupted initialization routine suspected.

---

## 5. ROM Extraction & Analysis

### 5.1 Procedure Overview

- External ROM chip identified on PCB.
- Controlled removal performed.
- ROM content extracted using specialized hardware interface.
- Raw binary dump acquired.
- Firmware structures analyzed at hex level.

> Exact extraction hardware and procedural specifics intentionally omitted.

---

### 5.2 Firmware Structure Review

Binary analysis revealed:

- Inconsistencies within system initialization modules.
- Abnormal data patterns within firmware parameter regions.
- Corrupted configuration blocks impacting startup sequence.

Hex-level inspection performed to validate structural anomalies.

![ROM Analysis Evidence](../evidences/case_002/case_002_rom_analysis.gif)

---

## 6. Firmware Integrity Correction

Structured firmware parameter correction was performed based on:

- Known-good firmware structure comparison.
- Checksum validation.
- Module integrity review.

Post-correction:

- Firmware lock condition resolved.
- Drive successfully completed initialization sequence.
- Full logical access restored.

---

## 7. Engineering Assessment

### Failure Mode
Firmware-level corruption affecting system modules responsible for drive initialization.

### Risk Considerations
- Improper firmware modification may permanently brick device.
- Checksum-protected structures require controlled validation.
- Recovery feasibility dependent on ROM integrity and adaptive data preservation.

---

## 8. Outcome

**Status:** Fully Recovered  
**Recovery Class:** Firmware-Level Intervention  
**Mechanical Condition:** Stable  
**Data Integrity:** Preserved  

---

## 9. Lessons & Technical Notes

- Firmware corruption can mimic mechanical failure symptoms.
- ROM extraction enables direct integrity validation.
- Structured firmware analysis must preserve adaptive data integrity.
- Controlled low-level access is critical in firmware-related recoveries.

---

[⬅ Back to Case Index](../README.md)
