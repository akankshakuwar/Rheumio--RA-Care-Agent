Agent Rheumio: Your Personal RA Care Buddy
​Agent Rheumio is an intelligent, empathetic AI companion designed specifically for individuals living with Rheumatoid Arthritis (RA). Unlike generic health bots, Rheumio understands the unpredictable nature of RA—adapting its advice on diet, exercise, and mental health based on the user's real-time pain levels and energy states.
​


🌟 The Problem
​Living   with RA means dealing with unpredictable pain, severe fatigue, and sudden flare-ups. Traditional health advice is often static and fails to account for "good days" vs. "bad days."
​Rheumio solves this by:
​Providing instant, personalized guidance.
​Remembering patient history (pain scores and energy levels).
​Filtering advice through strict safety guardrails (e.g., preventing heavy exercise during high-fatigue "Red" days).

​
🧠 System  Architecture
​Rheumio is built on a powerful Agentic Loop centered around the Google Gemini API. It moves beyond simple chat by utilizing Function Calling to interact with custom logic and state management.
​Technical Breakdown:
​The Brain: Powered by Gemini 2.5 Flash for high-speed reasoning and robust function calling.
​Persona & Guardrails: A deep system instruction set ensures an empathetic tone and enforces medical safety rules.
​The Tool Layer: Custom Python functions that allow the agent to:
​calculate_bmi(): Monitor physical health metrics.
​log_pain_score(): Track symptom severity over time.
​update_energy_meter(): Adjust the "State" of the agent to change its recommendation logic.
​Memory: Utilizes model.start_chat() to maintain a persistent conversation history, allowing the agent to act as a true long-term companion.


​🛠️ Tech Stack
​LLM: Google Gemini 2.5 Flash
​SDK: Google Generative AI Python SDK
​Environment: Kaggle Notebooks
​State Management: Session-based Python Global Variables
​Security: Kaggle Secrets for API Key Management


​🚀 How It Works: The Agentic Loop
​Input: User says, "I'm feeling very tired today, but I wanted to go for a run."
​Decision: Gemini recognizes the "tired" intent and calls update_energy_meter(state="Red").
​Execution: The system updates the internal state to "Red."
​Feedback: Gemini receives confirmation of the state change.
​Response: Based on safety guardrails for "Red" days, Rheumio responds: "Since your energy is low today, I strongly recommend skipping the run. Let's focus on gentle stretching or a 10-minute meditation instead."
​
🔮 Future Roadmap
​If developed further, Rheumio aims to move from reactive support to proactive flare prediction:
​Wearable Integration: Syncing with heart rate and sleep data via Google Cloud Healthcare API.
​Automatic Pacing: Automatically setting energy states based on biometric data.
​Predictive Modeling: Using ML to forecast flare probabilities 48 hours in advance.
​Mobile Deployment: Transitioning from a notebook prototype to a cross-platform mobile app.
​


🛠️ Setup & Usage
​Clone this repository.
​Ensure you have a Google Gemini API Key.
​Install dependencies: pip install -q -U google-generativeai
​Run the notebook cells to initialize the Rheumio agent.
