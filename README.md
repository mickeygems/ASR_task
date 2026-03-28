This project implements an end-to-end Automatic Speech Recognition (ASR) pipeline for Hindi speech, covering:

Data preprocessing
Whisper-based transcription
Text cleanup (numbers + code-switching)
Spelling quality analysis
Advanced evaluation using lattice-based WER

🧠 Key Features
 1. Whisper ASR Pipeline
Uses pretrained whisper-small
Handles audio + transcription pairing

 2. Number Normalization

Example:

तीन सौ पचास → 350

Handles:
Units, tens, multipliers
Avoids idiomatic phrases:
"दो-चार बातें" (unchanged)


 3. English Word Detection

Example:

मेरा इंटरव्यू अच्छा गया
→ मेरा [EN]इंटरव्यू[/EN] अच्छा गया
 
 4. Spelling Quality Analysis
Detects incorrect words using heuristics
Flags low-confidence words for review

 5. Lattice-based WER
    ["चौदह", "14"]

Allows multiple valid alternatives → fair evaluation

Instead of rigid reference:

["चौदह", "14"]

Allows multiple valid alternatives → fair evaluation
