# ✈️ AI Travel Assistant (AgentsVille)

A smart travel planning application powered by OpenAI LLMs. This system uses autonomous agents to generate, evaluate, and refine detailed travel itineraries based on user interests, weather conditions, and budget constraints.

## 🌟 Key Features
* **Structured Data:** Uses **Pydantic** models (`VacationInfo`, `TravelPlan`) to ensure strict JSON output and validation.
* **Multi-Agent Architecture:**
    * **Itinerary Agent:** Generates the initial day-by-day plan.
    * **Revision Agent:** Uses a **ReAct Loop** (Thought-Action-Observation) to iteratively fix issues.
* **Tool Integration:** The agents autonomously call Python tools (`calculator`, `weather_check`, `activity_finder`).
* **Robust Evaluation:** Includes automated logic to check for weather compatibility (e.g., avoiding outdoor events during rain) and budget limits.

## 🛠️ Tech Stack
* Python 3.x
* OpenAI API (GPT-4 / GPT-3.5)
* Pydantic (Data Validation)
* Jupyter Notebook

## 🚀 How it Works
1.  The user inputs vacation details (dates, interests, budget).
2.  The **Itinerary Agent** creates a draft plan.
3.  The **Revision Agent** loops through the plan, checking tools for weather/cost conflicts, and self-corrects the itinerary until it passes all checks.
4.  The system outputs a final validated JSON itinerary and a narrated audio summary.
