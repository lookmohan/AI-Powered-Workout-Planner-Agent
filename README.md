
# 🧠 AI-Powered Workout Planner Agent

This is an intelligent AI Agent built using **Langflow**, designed to generate personalized daily workout plans and nutrition tips based on user input like gender, weight, height, activity level, and fitness goals.

---

## 🧭 What Does This Project Do?

It creates a **fully customized 7-day workout plan** for users by analyzing their profile and fitness goals using an LLM (Mistral). It also provides **diet recommendations** and **training tips** to support their muscle gain journey.

---

## 🔧 How It Works (Workflow Overview)

The Langflow agent follows this logic:

1. **User inputs a request** like:  
   `"Can you generate a daily workout routine based on my goals?"`  
   and provides fitness details (e.g., male, 75kg, 176 cm, very active, gain weight).

2. **Prompt Template** → The LLM (Mistral) determines if the query is tool-based.

3. **Conditional Router** → Based on LLM output:  
   - ✅ If "Yes", it triggers a **ToolCallingAgent**.  
   - ❌ If "No", it sends a general LLM response.

4. **ToolCallingAgent** → Runs custom Python logic to generate a day-wise workout plan.

5. **ChatOutput** → Final response is displayed to the user.

---

## 🛠️ Technologies Used

| Tool         | Purpose                                  |
|--------------|------------------------------------------|
| Langflow     | No-code/low-code visual agent builder    |
| Mistral LLM  | LLM for decision-making and content      |
| Python       | Custom tool for workout plan generation  |
| ConditionalRouter | Logic control                       |
| Astra DB     | (Optional) for retrieval augmentation    |

---


📸 **Workflow Screenshot**![DataStax Langflow - Google Chrome 24-06-2025 14_36_14](https://github.com/user-attachments/assets/9f5c2d97-3de1-4f59-9f74-be6a4f2429f0)


## 🧑‍💻 How to Use This Project (For New Users)

### 1. Clone the Repo
```bash
git clone https://github.com/your-username/workout-planner-agent.git
cd workout-planner-agent
```

### 2. Install Langflow
```bash
pip install langflow
```

### 3. Launch Langflow
```bash
langflow run
```

### 4. Import the Flow
- Open your browser at `http://localhost:7860`
- Click **Import Flow**
- Upload the provided `Diet AI.json` file (or your own customized `.json`)

### 5. Run a Sample Query
Example:  
```
"Can you generate a daily workout routine based on my goals?"
male, 75kg, 176 cm, very active, goal: gain weight
```

You will see a complete workout plan and nutritional advice generated dynamically.

---

## 💡 What's Next?

I'm currently building a **frontend UI in Python (Streamlit or Flask)** to make this more user-friendly and accessible to non-technical users.

---

## 📄 License

MIT License – Free to use, share, and modify.
