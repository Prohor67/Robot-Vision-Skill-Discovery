# Robot-Vision-Skill-Discovery 🤖  


**Can robots learn just by watching?** This repository demonstrates how they can. Using only unlabeled videos, our pipeline discovers and interprets robotic manipulation skills—like grasping and placing—without any action labels or manually-crafted rewards.  


## 🔍 Project Overview  

Traditional robot learning often relies on **expert demonstrations** or **manually engineered reward functions**. But what if robots could **learn by simply observing videos**—just like humans?  

Our **unsupervised skill discovery pipeline** processes a single YouTube demonstration of a pick-and-place task and segments it into **16 distinct, semantically meaningful skills**. All of this is achieved **without supervision**, showing that scalable, video-driven robotic learning is possible.  


## 🛠️ Key Features  

- **Unsupervised Skill Segmentation:** Automatically detects transitions in behavior using Euclidean distance between consecutive visual embeddings.  
- **CLIP-Powered Embeddings:** Converts raw video frames into **512-dimensional semantic vectors** using a pre-trained CLIP image encoder.  
- **Automatic Skill Interpretation:** Matches discovered segments with textual action descriptions (e.g., *“Robot lifting object”*) using zero-shot text-image similarity.  
- **High Consistency:** Robust classification accuracy, especially for repetitive actions like object placement.  


## ⚙️ How It Works  

1. **Video Processing:** Extract and resize RGB frames from robot demonstration videos.  
2. **Feature Extraction:** Feed frames into CLIP to capture high-level visual semantics (robot poses and object interactions).  
3. **Skill Segmentation:** Identify points of significant behavioral change using a peak detection algorithm.  
4. **Semantic Labeling:** Assign human-readable labels to segments for interpretability.  


## 📊 Results  

The pipeline successfully identifies key manipulation stages such as:  

- **Approach & Grasp:** Moving toward objects, aligning the gripper, securing a grasp.  
- **Transport:** Lifting, carrying, and moving objects laterally.  
- **Placement & Retraction:** Lowering objects, releasing them, retracting the arm.  

✅ This shows robots can autonomously recognize **reusable, modular skills** from raw video input.  


## 🚀 Installation  

```bash
# Clone the repository
git clone https://github.com/yourusername/Robot-Vision-Skill-Discovery.git
cd Robot-Vision-Skill-Discovery

# Create a virtual environment
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows


