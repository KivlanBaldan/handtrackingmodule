# handtrackingmodule
A modular, object-oriented Python framework for real-time hand tracking and landmark detection using OpenCV and MediaPipe. Designed for easy integration into gesture control and human-computer interaction projects.
# Modular Hand Tracking System

A production-ready, object-oriented Python module designed for real-time hand detection, landmark tracking, and gesture boundary estimation. Powered by **OpenCV** and **Google's MediaPipe framework**, this codebase provides a lightweight API to integrate hand tracking into any computer vision pipeline with just a few lines of code.

---

## 🚀 Core Features

- **Real-Time Landmark Detection:** Maps 21 unique 3D hand coordinates (joints/fingertips) per hand at high frame rates.
- **Multi-Hand Support:** Configurable parameters to seamlessly detect and track single or multiple hands simultaneously.
- **Clean OOP Wrapper:** Built as an importable class structure (`HandDetector`) that abstracts away low-level processing configurations.
- **Coordinate Extraction:** Automated utility functions to fetch pixel coordinates $(x, y)$ of specific finger joints for downstream logic (e.g., gesture commands).

---

## 🖐️ Hand Landmark Reference Map
The underlying model maps 21 hand joints. You can target specific indices (e.g., `4` for Thumb Tip, `8` for Index Finger Tip) to build custom gesture triggers:

```text
    8    12    16    20
    |    |     |     |
    7    11    15    19
    |    |     |     |
    6    10    14    18
 4  |____|_____|_____|
  \ 5    9     13    17
   4     |     |     |
   |_____|_____|_____|
   3
   |
   2
    \
     1
      \
       0 (Wrist)
