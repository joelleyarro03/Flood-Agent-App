Panacea’s Passage is an AI-driven advisory tool for flood risk that leverages real-time weather information and
Gemini-based reasoning to identify possible flood areas and offer straightforward, comprehensible safety recommendations.
By examining precipitation patterns, temperature fluctuations, and various forecasting signals,
the system aids users in evaluating local flood hazards and making well-informed choices.
Constructed with a modular Flask backend and seamlessly integrated into Google Colab through secure API keys, 
this project showcases effective agent design, API integration, and analysis powered by large language models.

Flood-Agent-App/
│
├── app.py
├── requirements.txt
│
├── routes/
│   ├── agent.py
│   ├── health.py
│   ├── flood.py
│   ├── hospital.py
│   └── geocode.py
│
└── services/
    └── agent.py


Key Features
✅ Real-Time Weather Analysis

Integrates with the National Weather Service API

Processes short-term forecasts, precipitation probabilities, and more

Identifies location-based flood-zone risk patterns

🤖 Gemini-Powered Intelligence

Gemini serves as the main reasoning model

Produces technical JSON assessments

Generates clear explanations that residents can easily understand

🔁 Reinforcement Feedback

Users provide scores ranging from 1 to 5
Agent dynamically updates risk_sensitivity
Predictions evolve over time

🛡️ Fallback Simulation

Guarantees reliability when the weather API encounters rate limits or failures
🧩 Modular Architecture
Maintains a clean separation between logic (services/) and routes (routes/)
Facilitates easy debugging, testing, and extension

🌧️ Panacea’s Passage – AI Flood-Risk Advisory Agent

Powered by Gemini | Built with Flask | Utilizes Real-Time Weather Data

📌 Project Overview
Panacea’s Passage is an AI-driven flood-risk advisory platform aimed at analyzing weather predictions,
pinpointing potential flood-prone areas,
and conveying insights to users through concise, organized explanations. By assessing precipitation likelihood, 
temperature fluctuations, wind dynamics, and atmospheric conditions,
the system identifies regions that may be at a higher risk of flooding.

Gemini acts as the core reasoning model, providing technical evaluations and natural-language interpretations. 
Feedback in a reinforcement style enables the agent to enhance its risk sensitivity based on user feedback.
The system operates on a modular backend framework using Flask and integrates seamlessly with Google Colab via secure API key setups.

| Name                 | Role                                      | Email                                                                                           |
| -------------------- | ----------------------------------------- | ----------------------------------------------------------------------------------------------- |
| Williane Yarro   | Technical Developer  and github            | [willianeyarro03@gmail.com]                    |
| Jemima Egwurube  | Technical Developer / Integration Support |  [jemimaegwurube@gmail.com]
| Thien Nam Nguyen | Documentation Lead / Report Writer        |  [thienn15k@gmail.com] |
