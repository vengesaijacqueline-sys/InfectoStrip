# InfectoStrip System Architecture

## 1. System Overview

InfectoStrip is an AI-enabled point-of-care diagnostic platform that integrates a paper-based biochemical testing system with smartphone-based computer vision and artificial intelligence.

The system is designed to convert biological signals generated through diagnostic strip reactions into objective digital interpretations that support healthcare decision-making in low-resource settings.

The architecture consists of four interconnected layers:

1. Physical diagnostic layer — the InfectoStrip biochemical test platform.
2. Mobile application layer — the smartphone interface used for image capture and user interaction.
3. Artificial intelligence layer — the computer vision and machine learning system responsible for interpretation.
4. Healthcare decision-support layer — the interface through which healthcare workers receive and act on results.

---

# 2. Physical Diagnostic Layer: InfectoStrip Biochemical Test Platform

The foundation of InfectoStrip is a paper-based diagnostic strip designed for rapid point-of-care biochemical screening.

The strip contains multiple reaction zones containing specialised biochemical components capable of interacting with specific biomarkers present in biological samples.

When a patient sample is applied, biochemical reactions occur within these zones. These reactions generate measurable visual changes, primarily through changes in colour intensity and pattern formation.

Each reaction zone provides information related to specific biological markers associated with the targeted condition.

For the first product, InfectoStrip UTI Plus, the strip is being designed to support urinary tract infection screening by detecting relevant biochemical indicators associated with urinary tract infections.

The physical strip functions as the biological sensing component of the platform by converting invisible biological processes into measurable visual signals.

---

# 3. Smartphone Application Layer

The InfectoStrip mobile application acts as the connection between the physical diagnostic strip and the artificial intelligence system.

The application is designed to guide users through the testing workflow:

1. User selects the appropriate InfectoStrip test.
2. Patient sample is applied to the diagnostic strip.
3. The user captures an image of the completed strip using a smartphone camera.
4. The application performs image quality checks.
5. The captured image is processed and analysed by the AI system.
6. The interpreted result is displayed for healthcare decision support.

The application is designed for use by trained healthcare workers, including nurses and community health workers, who may operate in settings where access to laboratory specialists is limited.

Future versions may support community-based screening workflows where appropriate regulatory approval and safety requirements are met.

---

# 4. Artificial Intelligence Layer

The AI layer provides automated interpretation of the biochemical reaction patterns captured from the diagnostic strip.

The system uses computer vision and machine learning techniques to analyse the relationship between visual changes on the strip and clinically relevant screening outcomes.

## 4.1 Image Processing

Before interpretation, captured images undergo preprocessing to improve reliability.

Potential processing steps include:

- image quality assessment;
- detection of strip positioning;
- correction for lighting variation;
- colour normalisation;
- removal of image distortions.

These processes reduce the impact of differences caused by smartphone cameras, environmental lighting, and user handling.

---

## 4.2 Computer Vision Analysis

The computer vision model analyses features within the captured strip image, including:

- colour intensity changes;
- reaction zone patterns;
- spatial distribution of colour changes;
- relationships between multiple reaction areas.

The purpose of this analysis is to create a consistent interpretation process that reduces variability associated with manual visual comparison.

---

## 4.3 Machine Learning Interpretation

Machine learning models are used because real-world testing environments introduce variability that simple fixed colour thresholds may not handle effectively.

A rule-based system may perform poorly when images are affected by:

- different smartphone cameras;
- lighting conditions;
- background interference;
- variation in reaction strength.

Machine learning enables the system to learn patterns from representative training data and improve interpretation reliability across different operating environments.

The AI output will include:

- screening interpretation;
- confidence estimation;
- indication of when additional clinical review or confirmatory testing may be required.

---

# 5. End-to-End Data Flow Architecture
Patient Sample

    ↓

InfectoStrip Diagnostic Strip

(Biochemical Biomarker Reactions)

    ↓

Colour Pattern Generation

    ↓

Smartphone Camera Capture

    ↓

InfectoStrip Mobile Application

    ↓

Image Processing Pipeline

    ↓

AI Computer Vision Model

    ↓

Pattern Classification and Confidence Assessment

    ↓

AI-Assisted Screening Result

    ↓

Healthcare Worker Clinical Decision

---

# 6. Healthcare Worker Interaction Layer

InfectoStrip is designed as a clinical decision-support tool rather than an autonomous diagnostic replacement.

The healthcare worker remains responsible for:

- collecting patient history;
- performing clinical assessment;
- interpreting AI-assisted results within context;
- deciding whether additional testing or referral is required.

The AI system supports healthcare delivery by providing consistent interpretation of biochemical test results, particularly in environments where laboratory expertise may be limited.

---

# 7. Scalability Architecture

The long-term vision of InfectoStrip is to develop a modular diagnostic ecosystem where different disease-specific strips operate through a shared digital platform.

The same architecture can support additional InfectoStrip products, including potential future applications such as:

- InfectoStrip TB;
- InfectoStrip Febrile;
- InfectoStrip Maternal;
- InfectoStrip Sepsis.

Each diagnostic strip would contain disease-specific biochemical detection components, while the mobile application and AI interpretation framework provide a common digital infrastructure.

This approach allows expansion across multiple healthcare challenges without requiring healthcare workers to learn entirely new digital workflows for every diagnostic application.

---

# 8. Current Development Status

The InfectoStrip architecture is currently being developed as a prototype framework.

Current development priorities include:

- refining the diagnostic strip design;
- developing the mobile application workflow;
- building and validating AI interpretation models;
- establishing appropriate testing and regulatory pathways.

Before clinical deployment, InfectoStrip will require laboratory validation, ethical review, regulatory approval, and clinical evaluation.
