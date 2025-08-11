🍗 Wings R Us – AI‑Powered Checkout Recommender
💡 Introduction
Wings R Us, a fast‑growing Quick Service Restaurant (QSR) chain in the USA, wanted to supercharge its digital ordering experience and boost Average Order Value (AOV).
This project delivers a smart, hybrid recommendation engine that understands who the customer is and what they're most likely to buy next.

📌 Highlights

Hybrid AI – Combines market basket analysis + personalized filtering

Context‑aware logic – Different engine for guest vs registered users

End‑to‑end pipeline – From raw data cleaning to a deployed interactive app

Explainable recommendations – Powered by Gemini API

🌐 Live Demo & Assets
Interactive Streamlit App → Try It Here

Power BI Dashboard → WWT_dashboard.pbix (Requires Power BI Desktop)

📂 Project Files
File	Purpose
Data_Cleaning.ipynb	Prepares and merges datasets; fixes nulls; parses nested JSON
EDA.ipynb	Exploratory analysis; RFM customer segmentation; business findings
Recommendation.ipynb	Builds FP‑Growth & Collaborative Filtering models; exports .joblib
App.py	Streamlit frontend for end users
guest_fp_growth_model.joblib	Pretrained frequent‑itemset model for guest users
loyal_collab_filtering_model.joblib	Pretrained collaborative filter for registered customers
requirements.txt	Python package list
.env	Holds API key for Gemini (excluded from GitHub)
⚙️ Quick Setup
1️⃣ Get the Code
bash
git clone <your-repository-url>
cd <repository-folder>
2️⃣ Environment Setup
bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
3️⃣ Install Dependencies
bash
pip install -r requirements.txt
4️⃣ Add API Key
Create .env in the root folder:

text
GEMINI_API_KEY="your_api_key_here"
▶️ Running the App
Option A – Use provided pretrained models (fast)

bash
streamlit run App.py
Option B – Retrain from scratch (slower)

Run Data_Cleaning.ipynb → produces final_merged_data.csv

Run EDA.ipynb for segmentation + insights

Run Recommendation.ipynb to generate .joblib models

Launch Streamlit as in Option A

🧠 How It Works
👤 Guest Users → FP‑Growth Market Basket
Detects items bought together frequently

Works without prior customer history

Example: "Customers who order Spicy Wings often grab Ranch Dip too."

🔐 Registered / eClub Users → Collaborative Filtering
Learns from purchase history to find “look‑alike” items

Tailors suggestions to personal taste

Example: "You love spicy options – here’s a new fiery flavor you haven’t tried yet."

📊 Business Insights Discovered
AOV Surprise – Guests: $53.15 vs Loyal Customers: $39.29

Dual‑speed market – Mix of high‑spend first‑timers + steady regulars → hybrid model is ideal

Geographic skew – Strong presence in Texas; room for geo‑personalized promos

🚀 Tech Stack
Python | Pandas | Scikit‑learn | FP‑Growth | Surprise Library | Streamlit | Gemini API | Power BI

💬 Built to turn every checkout into a bigger basket and a better experience!

## 📝 License
This project is for academic/demo purposes. Adapt and use freely.

---

## 🙌 Credits
Built using Python, Streamlit, and Gemini AI ✨


<img width="1331" height="866" alt="image" src="https://github.com/user-attachments/assets/eee78d70-7aa9-451b-881c-7ac032eb68f9" />

