# Stock Market Analysis AI Agent 📊

## Overview 🎯
An AI-powered agent that fetches stock market indices, analyzes trends, and sends push notifications with financial insights to registered Android devices.

## Features 🚀
- Fetch real-time stock market indices
- Analyze market trends (Bullish, Bearish, Neutral)
- Generate financial quotes based on market performance
- Send push notifications via Firebase Cloud Messaging (FCM)
- REST API for data retrieval and device registration
- Simple Android app for notifications

## Tech Stack 🛠️
| Component         | Tech Used                         |
|------------------|---------------------------------|
| Backend API      | FastAPI / Flask / Node.js       |
| Stock Data API   | Alpha Vantage / Yahoo Finance  |
| Database         | PostgreSQL / Firebase Firestore |
| Scheduler        | Celery + Redis / APScheduler   |
| Notifications    | Firebase Cloud Messaging (FCM) |
| Mobile App       | React Native / Flutter         |
| Hosting         | AWS / Google Cloud / Heroku    |

## Architecture 🏗️
```
[Stock Market API] -> [Backend] -> [Market Analysis] -> [Financial Insights] -> [FCM Push Notifications] -> [Android App]
```

## Project Structure 📂
```
Stock-Market-AI-Agent/
│── backend/
│   ├── main.py          # API Server
│   ├── scheduler.py     # Job Scheduling
│   ├── analysis.py      # Market Analysis
│   ├── notifications.py # Push Notifications
│   ├── config.py        # Configuration
│── mobile-app/
│   ├── src/
│   │   ├── App.js       # Main React Native App
│   │   ├── screens/     # UI Screens
│   │   ├── services/    # Firebase Integration
│── database/
│   ├── models.py        # Database Schema
│   ├── queries.py       # CRUD Operations
│── requirements.txt     # Python Dependencies
│── package.json         # React Native Dependencies
│── .env                 # Environment Variables
```

## Development Workflow 🔄
1. **Fetch Stock Data**: Retrieve real-time stock indices at intervals.
2. **Analyze Trends**: Categorize into Bullish, Bearish, Neutral.
3. **Generate Insights**: Assign financial quotes based on trends.
4. **Send Notifications**: Push alerts via FCM to Android devices.
5. **API Development**: Provide REST endpoints for data retrieval.
6. **Mobile App**: Handle push notifications and display market insights.

## 🔍 Breaking Down the Problem

### 🏛 Sub-Problem 1: Fetching Stock Market Index Data
- Retrieve real-time stock data at predefined intervals.
- Store data for further analysis.

### 📊 Sub-Problem 2: Analyzing Index Performance
- Determine whether the trend is Bullish, Bearish, or Neutral.
- Use statistical techniques like SMA & RSI.

### 💡 Sub-Problem 3: Generating Financial Insights
- Select and assign relevant financial quotes dynamically.
- Ensure quote relevance based on trend classification.

### 📩 Sub-Problem 4: Sending Push Notifications
- Register and manage device FCM tokens.
- Automate notifications based on stock movement insights.

### 🌐 Sub-Problem 5: Backend API Development
- Develop a REST API for data retrieval and notification management.

### 📱 Sub-Problem 6: Android App Development
- Implement Firebase push notifications in Android.
- Develop a UI to display market insights & historical notifications.



## Installation & Setup ⚙️
### Backend Setup 🖥️
```bash
# Clone repo
git clone https://github.com/Prabhukiran161/Stock-Market-Analysis-AI-Agent.git
cd Stock-Market-Analysis-AI-Agent

# Create virtual environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run the server
uvicorn main:app --reload
```
### Android App Setup 📱
1. Open the project in **Android Studio**.
2. Add `google-services.json` to the `app/` directory.
3. Build and run the app.

## API Endpoints 🌐
| Endpoint            | Method | Description                    |
|--------------------|--------|--------------------------------|
| `/get_market_data` | GET    | Fetch latest stock market data |
| `/register_device` | POST   | Register a device with FCM     |
| `/send_notification` | POST  | Send push notifications        |

## Future Enhancements 🔮
- Machine Learning-based stock trend prediction
- Web dashboard for visualization
- Custom user preferences for indices

## Contributors 🤝
- **[Your Name]** - Developer

## License 📜
Licensed under the **MIT License**.

