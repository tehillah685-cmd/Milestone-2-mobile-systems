#  Appendix: BioPulse Usability Evaluation & Empirical Results

This appendix documents the experimental methodology, task protocols, raw quantitative metrics, and survey evaluation instruments used to assess the BioPulse mobile system prototype.

---

## A.1 Experimental Evaluation Design
Because this assignment focuses on UI/UX design, physical wearable hardware (the BioPulse SkinGrip patch) was simulated using interactive prototype triggers:
* **NFC Pairing:** Simulated via interactive tap triggers mimicking smartphone-wearable contact
* **Biometric Disarm:** Evaluated via device-native Face ID / Touch ID verification overlays
* **Participant Cohort ($N = 3$):** Users were selected to represent the three target persona archetypes (Sarah Williams, Michael Chen, and Margaret Taylor)

---

## A.2 Raw Quantitative Usability Telemetry

| Participant ID | Target Persona Profile | Task 1: NFC Pairing Time (s) | Task 3: Biometric Disarm Time (s) | Task Completion Rate | System Usability Scale (SUS) Score |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **User 1** | Vulnerable Commuter  | 1.9s | 1.5s | 100% | 90.0 / 100 |
| **User 2** | Independent Traveller  | 2.3s | 1.8s | 100% | 87.5 / 100 |
| **User 3** | Independent Senior  | 2.1s | 2.0s | 100% | 87.0 / 100 |
| **Mean Average** | — | **2.1s** | **1.8s** | **100%** | **88.2 / 100** |

---

## A.3 Qualitative Participant Observations

* **User 1 (Vulnerable Commuter Profile):**
  > *"The 5-second countdown screen is striking, but having Face ID immediately pop up to cancel false alarms makes you feel in complete control. You don't have to panic about typing a PIN code."
* **User 2 (Independent Traveller Profile):**
  > *"The green monitoring dashboard gives great peace of mind. You can tell instantly at a glance that the app is actively running in the background."
* **User 3 (Independent Senior Profile):**
  > *"The text size and button contrast are excellent. Simulating the NFC patch tap was very easy—much better than trying to pair Bluetooth devices manually."

---

## A.4 System Usability Scale (SUS) Questionnaire Instrument
Users responded to the following 10 standard items on a 5-point Likert scale (1 = Strongly Disagree, 5 = Strongly Agree):
1. I think that I would like to use this system frequently for my personal safety.
2. I found the system unnecessarily complex. 
3. I thought the system was easy to use
4. I think that I would need the support of a technical person to be able to use this system. *(Reverse Scored)*
5. I found the various functions in this system were well integrated[cite: 32].
6. I thought there was too much inconsistency in this system. *(Reverse Scored)*
7. I would imagine that most people would learn to use this system very quickly[cite: 32].
8. I found the system very cumbersome to use. *(Reverse Scored)*
9. I felt very confident using the system[cite: 32].
10. I needed to learn a lot of things before I could get going with this system. *(Reverse Scored)*
