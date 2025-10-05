🤖 Custom AI Agent Builder
This project provides a simple, single-file web application that serves as a flexible framework for building custom AI agents using the Gemini API. It allows users to control the agent's Persona, Task, and Output Structure (JSON or standard text).

This project was built step-by-step to demonstrate core concepts of modern LLM application development.

✨ Features
Dual-Mode Agent: Easily switch between two primary agent modes:

Grounded Analysis: Uses Google Search (Tooling) to provide current, sourced, high-quality text answers.

Structured Extraction: Enforces strict JSON output based on a user-defined schema for clean data extraction (disables search due to a model constraint).

Custom Persona: Define the agent's tone, role, and rules via a System Instruction.

Adaptive UI: The single HTML file features a responsive design that automatically adapts to the user's system dark or light theme.

Robust Error Handling: Includes logic for API key validation and catching common 400 Bad Request errors.

⚙️ How to Run Locally
1. Prerequisites
You must have a Gemini API Key.

2. File Setup
This project uses a single file, which you have created in your local repository (AI_Agent/agent_builder.html).

3. Insert Your API Key
Open the agent_builder.html file in your text editor (VS Code is recommended). Navigate to the JavaScript section (around line 139) and replace the placeholder with your actual key:

// --- 1. API Configuration (API Key Required Here) ---
const MODEL_NAME = "gemini-2.5-flash-preview-05-20";
// *** IMPORTANT: INSERT YOUR GEMINI API KEY HERE ***
const apiKey = "YOUR_API_KEY_HERE"; // <-- REPLACE THIS WITH YOUR KEY!
const apiUrl = `https://generativ语言.googleapis.com/v1beta/models/${MODEL_NAME}:generateContent?key=${apiKey}`;

4. Launch the Application
Double-click the agent_builder.html file in your operating system, or open it in VS Code and use the "Open with Live Server" extension.

🚀 How to Use the Agent
Try these two different modes to see the agent's full capabilities:

Mode A: Grounded Text Output (Enables Search)
Set Output Type to Standard Text Output (Markdown).

System Instruction (Persona): You are a satirical movie critic who writes overly dramatic, five-sentence reviews.

User Prompt (Task): Review the latest blockbuster film, Oppenheimer.

Result: You get a dramatic, five-sentence review using real-time search data, along with source citations.

Mode B: Structured JSON Output (Disables Search)
Set Output Type to Structured JSON Output (Guaranteed).

System Instruction (Persona): Your only task is to extract information and return it in the provided JSON format.

JSON Response Schema: Use the default schema provided in the input box.

User Prompt (Task): List three common dog breeds and their average adult weight in kilograms.

Result: You get perfectly clean, parsable JSON data.
