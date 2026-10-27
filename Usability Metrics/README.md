# BioPulse — Usability & System Evaluation Dataset

This directory contains the raw empirical usability data, task performance metrics, and System Usability Scale (SUS) survey responses collected during the Milestone 2 evaluation of the **BioPulse** Mobile Emergency and Biometric Safety System.

---

## 📄 Dataset Overview

* **Filename:** `biopulse_usability_results.csv`
* **Sample Size ($N$):** 3 participants (representing the core target user persona profiles)
* **Methodological Frameworks:**
  * **PACMAD Usability Model** (Harrison et al., 2013; Lazar, 2024) — Evaluating Effectiveness, Efficiency, Learnability, and User Error Protection under dynamic mobile contexts.
  * **ISO/IEC 25010:2023 Product Quality Standard** (ISO, 2023) — Focus on Interaction Capability, Functional Correctness, and User Satisfaction under simulated high-stress emergency conditions.

---

## 👥 Participant Cohort Profiles

| Participant ID | Persona Profile Represented | Key Evaluation Focus |
| :--- | :--- | :--- |
| **User 1** |  (Vulnerable Commuter) | Panic disarm speed, countdown cognitive friction, and emotional reassurance post-incident. |
| **User 2** | (Independent Traveller) | Technical clarity, live GSR telemetry visualization, and status transparency. |
| **User 3** | (Independent Senior) | Visual accessibility, large touch targets, NFC setup ease, and error prevention. |

---

##  Test Case Protocols (TC1 – TC4)

1. **TC1: Hardware Coupling (NFC Tap-to-Pair)**
   * *Task:* Initialize wireless pairing between smartphone and SkinGrip patch via single NFC tap gesture.
   * *Target Benchmark:* $< 3.0$ seconds completion.
2. **TC2: Visual Telemetry Audit**
   * *Task:* Audit active connection status, battery percentage, and live GSR bio-signal graph on main dashboard (`1.png`).
   * *Target Benchmark:* $< 2.0$ seconds visual processing time.
3. **TC3: Biometric False-Alarm Disarm**
   * *Task:* Cancel active 5-second emergency countdown using native Face ID / Touch ID biometric authentication (`7.png`, `8.png`).
   * *Target Benchmark:* $< 3.0$ seconds disarm execution.
4. **TC4: Emergency Escalation Verification**
   * *Task:* Verify automated GPS packaging, 911 RapidSOS notification, and incident location display on active emergency screen (`10.jpg`).
   * *Target Benchmark:* $< 5.0$ seconds automated dispatch.

---

##  Summary Results & Data Implications

### Task Performance Metrics

| Test Case | Metric Evaluated | Mean Result ($N=3$) | Target Benchmark | Outcome |
| :--- | :--- | :--- | :--- | :--- |
| **TC1** | Mean Time-on-Task | **2.1s** | $< 3.0$s | **PASS** (100% Completion) |
| **TC2** | Visual Processing Time | **1.2s** | $< 2.0$s | **PASS** (100% Completion) |
| **TC3** | Mean Disarm Latency | **1.8s** | $< 3.0$s | **PASS** (3.2s Safety Margin) |
| **TC4** | Automated Dispatch | **4.5s** | $< 5.0$s | **PASS** (100% Automated) |

### System Usability Scale (SUS) Scores

* **User 1:** 90.0 / 100 (*Grade A+ / Best Imaginable*)
* **User 2:** 87.5 / 100 (*Grade A / Excellent*)
* **User 3:** 87.0 / 100 (*Grade A / Excellent*)
* **Mean Overall SUS:** **88.2 / 100** (*Grade A — Top 5th Percentile Usability*)

---

##  CSV Data Schema Definition

The raw CSV file (`biopulse_usability_results.csv`) is structured with the following fields:

* `participant_id`: Unique identifier for test subject (`User_1`, `User_2`, `User_3`)
* `persona_profile`: Mapped persona profile (*Vulnerable Commuter*, *Independent Traveller*, *Independent Senior*)
* `tc1_nfc_pairing_time_sec`: Time in seconds to complete NFC pairing
* `tc1_nfc_taps_count`: Total tap actions required
* `tc1_success`: Boolean task completion flag (`TRUE`/`FALSE`)
* `tc2_telemetry_audit_time_sec`: Visual processing duration for dashboard status
* `tc2_success`: Boolean task completion flag (`TRUE`/`FALSE`)
* `tc3_biometric_disarm_time_sec`: Time in seconds to disarm threat alert via Face ID / Touch ID
* `tc3_disarm_actions_count`: Biometric scan attempts required
* `tc3_success`: Boolean task completion flag (`TRUE`/`FALSE`)
* `tc4_emergency_dispatch_time_sec`: Automated emergency pipeline execution time
* `tc4_success`: Boolean task completion flag (`TRUE`/`FALSE`)
* `sus_q1` to `sus_q10`: Raw responses (1–5 Likert scale) for standard System Usability Scale questions
* `sus_final_score`: Computed SUS total out of 100
