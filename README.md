# HRAI_MEF 
## An LLM powered robot assistant for the Italian Ministry of Economy and Finance

MEF-Bot is a Human-Robot Interaction (HRI) system built on the **G1 humanoid 
robot** developed for the HRAI course project held in Sapienza University of Rome. 
The system simulate the deploy of Unitree G1 as a conversational assistant in a real 
public administration office, the Italian Ministry of Economy and Finance (MEF).

## 🏛️ Context
Public administration offices represent one of the most socially and 
institutionally significant environments in which to study human-robot 
interaction. Unlike controlled lab settings, a real PA office brings 
together users across a wide range of ages, technical literacy levels, and interaction expectations. 
This makes it a  uniquely valuable testbed not only for robotics and AI engineering, but also for 
understanding how people perceive, trust, and adapt to AI-powered robots in 
high-stakes institutional contexts.

From a social sciences perspective, the deployment raises meaningful questions: 
How the physical presence of a robot shape user trust and compliance compared to a screen-based chatbot? 
How do professional norms and power dynamics in a bureaucratic environment influence human-robot interaction 
patterns? How do people negotiate authority and agency when a robot mediates 
access to information? MEF-Bot is designed as a real-world probe into these 
questions.

## 🎯 Use Cases
- **Office Worker Assistant**: Employees query the robot in natural Italian 
  to retrieve administrative documents, forms, and procedures
- **Visitor & Employee Reception**: The robot greets and guides visitors, 
  identifies their needs, and provides onboarding information to new employees.
  
## 🤖 System Overview

The architecture follows the **companion server pattern**: The humanoid handles 
audio capture, speech output, gesture, LED feedback, and tablet display, 
while more expensive AI computation runs on a local server connected via LAN.

**Core pipeline:**
- **ASR**: Automatic Speech Recognition to convert italian spoken audio into written text;
- **LLM**: Off/On-premise LLM model as the reasoning engine with a context-specific system prompt
- **RAG**: Retrieval-Augmented Generation over a knowledge base of ministry documents;
- **Navigation**: Walk avoiding obstacles with pre-built laser map and 
  defined waypoints



## ⚖️ License
This project is released under:

CC BY-NC 4.0 — Attribution required, commercial use is not allowed.

© 2026 [Alessandro Massari]


