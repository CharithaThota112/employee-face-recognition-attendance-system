Employee Face Recognition Check-In / Check-Out System
An intelligent employee attendance and access management system that uses computer vision, facial recognition, liveness detection, and role-based access control to automate secure employee check-in and check-out.

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-red?style=for-the-badge&logo=opencv)
![CNN](https://img.shields.io/badge/CNN-Facial%20Recognition-orange?style=for-the-badge)
![MTCNN](https://img.shields.io/badge/MTCNN-Face%20Detection-green?style=for-the-badge)
![MySQL](https://img.shields.io/badge/MySQL-Database-blue?style=for-the-badge&logo=mysql)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

 Overview

The **Employee Face Recognition Check-In / Check-Out System** is a computer vision-based attendance management platform designed to automate employee attendance while providing an additional layer of authentication and access control.

The system captures an employee's face through a camera, performs image preprocessing, detects and aligns the face, verifies liveness, extracts facial features, and matches them against registered employee data.

After successful recognition, the system identifies the employee's role and applies **Role-Based Access Control (RBAC)** before allowing attendance operations.

The system records check-in/check-out timestamps and generates attendance information that can be used for analytics and reporting.

 Objectives

The main objectives of the project are:

- Automate employee attendance using facial recognition.
- Reduce manual check-in/check-out processes.
- Provide secure employee authentication.
- Detect live users using liveness verification.
- Prevent unauthorized attendance operations.
- Implement role-based access control.
- Record accurate check-in and check-out timestamps.
- Classify attendance based on defined time rules.
- Provide attendance analytics and reports.
- Improve face recognition reliability under varying lighting conditions.
- Support real-time computer vision processing.

 Key Features

 1. Face Detection

The system uses **MTCNN (Multi-task Cascaded Convolutional Networks)** for detecting faces from the camera input.

It identifies facial regions before further recognition and authentication steps are performed.

 2. Image Preprocessing

The captured image is processed before recognition to improve the quality and reliability of face detection.

Preprocessing includes:

- Image resizing
- Noise reduction
- CLAHE-based contrast enhancement
- Illumination normalization
- Face alignment

These techniques help improve recognition performance when employees are captured under different lighting conditions.

 3. Facial Recognition

After detecting and aligning the face, the system extracts facial features and generates a facial representation/embedding.

The extracted features are compared with registered employee facial data to identify the employee.

```text
Camera Input
     ↓
Face Detection
     ↓
Face Alignment
     ↓
Feature Extraction
     ↓
Facial Embedding
     ↓
Feature Matching
     ↓
Employee Identification

Testing

The system was tested against different scenarios to verify the major components of the application.

Test Case 1 — Registered Employee

Input: Registered employee's face.

Expected Result:
The employee is recognized and authorized attendance is recorded.

Test Case 2 — Unknown Employee

Input: Unregistered face.

Expected Result:
The system rejects authentication and does not record attendance.

Test Case 3 — Liveness Verification Failure

Input: Non-live/static face representation.

Expected Result:
The liveness check fails and the attendance process is stopped.

Test Case 4 — Different Lighting Conditions

Input: Face captured under different lighting conditions.

Expected Result:
Preprocessing techniques improve the quality of the input and assist face detection and recognition.

Test Case 5 — Unauthorized Operation

Input: Recognized user without the required permission.

Expected Result:
RBAC prevents the unauthorized operation.

Challenges & Solutions
Challenge 1 — Face Detection Under Different Lighting

Face detection and recognition can become difficult when lighting conditions change.

Solution

The preprocessing pipeline was enhanced using:

CLAHE contrast enhancement
Illumination normalization
Noise reduction
Image resizing

These steps improve the quality of the input before face recognition.

Challenge 2 — Spoofing / Non-Live Face

A face recognition system can potentially accept a photograph or other non-live representation.

Solution

Liveness detection was incorporated using:

Eye-blink verification
Head-movement verification

The system proceeds with authentication only after the liveness condition is satisfied.

Challenge 3 — Access Control

Different users should have different permissions within the system.

Solution

Role-Based Access Control (RBAC) was implemented to validate the employee's role and permissions before performing protected operations.

 Project Status

Status: Completed Academic Project

The system demonstrates an automated approach to employee attendance using facial recognition, liveness verification, and role-based access control.
License

This project is created for educational and portfolio purposes.
Further improvements can be made through advanced anti-spoofing, cloud integration, mobile support, and enhanced analytics.
