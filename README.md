# 🚨 VIT Campus Rescue Simulator  
*A multi-agent Q-learning simulation for search-and-rescue missions in a university campus.*



## 📖 Overview  
This project simulates a **multi-agent rescue mission** on the VIT Bhopal campus using **Q-learning** (a reinforcement learning technique). Autonomous agents navigate a 50×50 meter grid to locate and rescue victims while avoiding obstacles.

**Key Features:**  
- **Q-learning-based pathfinding** with customizable parameters (learning rate, exploration, etc.)  
- **Interactive Folium map** visualizing agent paths, victims, and obstacles  
- **Real-time metrics** (battery, distance covered, rescue count)  
- **Streamlit web UI** for easy control and visualization  

---

## 🛠️ Installation  
1. **Clone the repository:**  
   ```bash
   git https://github.com/Ainirzv/MARL-for-rescue-and-search.git
   ```

2. **Install dependencies:**  
   ```bash
   pip install streamlit numpy pandas folium streamlit-folium
   ```

3. **Run the simulation:**  
   ```bash
   streamlit run app.py
   ```

---

## 🎮 Usage  
1. **Set up the mission:**  
   - Configure victim/obstacle locations in the sidebar.  
   - Adjust Q-learning parameters (learning rate, exploration, etc.).  

2. **Start the simulation:**  
   - Click **"Start Mission"** to begin. Agents autonomously navigate using Q-learning.  

3. **Monitor progress:**  
   - Real-time map updates show agent paths (colored lines).  
   - Status table tracks battery, rescues, and distance covered.  

4. **Reset:**  
   - Click **"Reset Mission"** to clear all agents and targets.  

---

## 🧠 How It Works  
### 🔄 Q-Learning Implementation  
- **State Space:** Discrete 2-meter grid positions.  
- **Actions:** 8 possible directions (2 meters per step).  
- **Rewards:**  
  - `+100` for rescuing a victim.  
  - `-50` for hitting an obstacle.  
  - `+5` for moving closer to the nearest victim.  

### 🌍 GPS Mapping  
- Campus coordinates are converted to GPS (centered at VIT Bhopal).  
- Folium visualizes agents, paths, and obstacles on an OpenStreetMap.  

---

## 📊 Example Output  
![Screenshot](https://github.com/Ainirzv/MARL-for-rescue-and-search/blob/main/marl.jpg) *(Replace with actual screenshot)*  

**Status Table:**  
| Agent    | Status      | Battery | Distance | Rescues | Position  | Time   |  
|----------|-------------|---------|----------|---------|-----------|--------|  
| rescue1  | 🏁 Reached  | 45.2%   | 32m      | 2       | (25, 40)  | 18.3s  |  

---

## 📂 File Structure  
```
Rescue/
├── app.py  # Main simulation code
├── README.md            
└── requirements.txt     # Dependencies 
```

---

## 🤝 Contributing  
Contributions are welcome! Open an issue or submit a PR for:  
- Improved Q-learning algorithms.  
- Additional visualization features.  
- Performance optimizations.  

---

## 📜 License  
[MIT](https://choosealicense.com/licenses/mit/)  



