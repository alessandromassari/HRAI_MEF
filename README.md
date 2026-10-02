# HRAI_MEF 
## An LLM powered robot assistant for the Italian Ministry of Economy and Finance

MEF-Bot is a Human-Robot AI Interaction (HRI) system built on the **G1 humanoid 
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
- **Office Worker Assistant**: Users query the robot in natural language
  to retrieve administrative documents, forms, and procedures
- **Visitor & Employee Reception**: The robot greets and guides visitors, 
  identifies their needs, and provides onboarding information to new employees.
  
## 🤖 System Overview
The architecture combines LLM-based task interpretation, persistent semantic perception, symbolic semantic relations, classical path planning and Reinforcement Learning for humanoid locomotion.

**Main components:**
- **Persistent Semantic perception**: RGB-D observations are processed to detect, segment, localise and associate objects across different viewpoints;
- **LLM**: Off/On-premise LLM model as the reasoning engine with a context-specific system prompt
- **LOST-3DSG open vocabulary semantic mapping**: A customized version of the work presented in LOST-3DSG paper provides the main conceptual reference for the persistent object-centric world representation;
- **Navigation**: Walk avoiding obstacles over an occupancy map built during 'exploration' phase;
- **MuJoCo & MJLab**: provides the simulated humanoid platform and physical environment.

## 🧪 Experimental Evaluation
The system was evaluated through separate navigate, locate, and describe tasks using multiple linguistic formulations and semantic targets.

The evaluation considers:

- intent recognition;
- semantic grounding;
- task success;
- response correctness and grounding;
- navigation execution;
- inference and end-to-end latency.

## How to use
Clone the repository with: 
```bash
git clone --recursive <URL_DEL_PROGETTO_PRINCIPALE>
```
From terminal, only the first time:
```bash
chmod +x init_env.sh start.sh
./init_env.sh
```
All times after to start the Docker:
```bash
./start.sh
```
The main HRAI application is launched through:
```bash
cd /workspace/exchange/interaction
python3 HG1AI_interaction.py
```
## ⚖️ License
This project is released under:

CC BY-NC 4.0 — Attribution required, commercial use is not allowed.

© 2026 [Alessandro Massari]


