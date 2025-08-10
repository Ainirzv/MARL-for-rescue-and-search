Here's a clean, copyable `README.md` for your GitHub repository. Simply copy and paste this into a new `README.md` file in your project:

```markdown
# 🚨 VIT Campus Rescue Simulator  
*A multi-agent Q-learning simulation for search-and-rescue missions on a university campus*

![Demo Screenshot](demo_screenshot.png)  
*(Replace with actual screenshot path after uploading)*

## 📖 Overview
This Streamlit-based simulator models autonomous rescue agents navigating a 50×50 meter campus grid to locate victims while avoiding obstacles. Agents learn optimal paths using **Q-learning reinforcement learning**.

## 🚀 Features
- **Interactive Folium map** with real-time agent tracking
- **Customizable parameters**:
  - Victim/obstacle locations
  - Learning rate, discount factor, exploration rate
- **Multi-agent coordination** (5 agents by default)
- **Battery & performance metrics** for each agent

## ⚙️ Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Premkolte/Rescue.git
   cd Rescue
   ```

2. Install dependencies:
   ```bash
   pip install streamlit numpy pandas folium streamlit-folium
   ```

3. Run the simulation:
   ```bash
   streamlit run rescue_simulator.py
   ```

## 🎮 Usage
1. **Configure mission** in the sidebar:
   - Set victim/obstacle locations
   - Adjust Q-learning parameters

2. **Start simulation**:
   - Click "Start Mission"
   - Agents autonomously explore using Q-learning

3. **Monitor results**:
   - Real-time map updates
   - Agent status table (battery, rescues, etc.)

4. **Reset** anytime with "Reset Mission"

## 🧠 Technical Details
### Q-Learning Implementation
| Component          | Specification                          |
|--------------------|----------------------------------------|
| State Space        | Discrete 2-meter grid positions        |
| Actions            | 8 directions (2m/step)                |
| Rewards            | +100 (rescue), -50 (obstacle), +5 (moving closer) |
| Learning Rate      | Adjustable (default: 0.1)              |

### GPS Mapping
- Campus centered at VIT Bhopal coordinates (23.2745°N, 77.4185°E)
- 50×50 meter area visualized using Folium

## 📊 Expected Output
After successful simulation:
```
Mission Completion: 100%
All campus victims rescued!

Agent Status:
| Agent    | Status      | Battery | Distance | Rescues |
|----------|-------------|---------|----------|---------|
| rescue1  | 🏁 Reached  | 52.1%   | 28m      | 2       |
```

## 🤝 Contributing
Contributions are welcome! Please open an issue or PR for:
- Enhanced visualization
- Algorithm improvements
- Additional metrics

## 📜 License
MIT License
```

**To use this README:**
1. Copy the entire content above
2. Create a new file named `README.md` in your project root
3. Paste the content
4. Replace `demo_screenshot.png` with an actual screenshot path after uploading one
5. Customize any sections as needed

The formatting uses standard GitHub Markdown and includes:
- Clear section headers
- Code blocks for commands
- Tables for technical specs
- Emoji for visual organization
- Placeholder for your demo image

Would you like me to add any specific details about the Q-learning implementation or Streamlit components?
