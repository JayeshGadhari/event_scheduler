# 🗓 Event Scheduler API

A simple Python + Flask project to create, list, update, and delete calendar events.  
This project uses a JSON file for storage and is perfect as a small backend or for learning REST APIs.

---

## 🚀 How to run the project

1️⃣ Clone this repository or unzip the project folder locally.

2️⃣ Install dependencies:
```bash
pip install -r requirements.txt


3️⃣ Make sure your events.json file exists and contains at least an empty list:
[]

4️⃣ Start the Flask server:
```bash
python app.py


The API will be available at:
http://127.0.0.1:5000


📦 Project structure:
```bash
event_scheduler/
├── app.py                                 # Flask app with API endpoints
├── storage.py                             # Helper to load/save events from JSON
├── events.json                            # Data file to store events (keep [] inside)
├── requirements.txt                       # Python dependencies (Flask)
├── README.md                              # Project documentation (this file)
└── Event Scheduler.postman_collection.json  # Postman collection to easily test the API


🧪 How to test using Postman
You don’t need to build a frontend — just use Postman:

1️⃣ Open Postman → click Import
2️⃣ Select the file: Event Scheduler.postman_collection.json
3️⃣ Use the saved requests inside the collection to test your API:

| Method |             Endpoint |                             Description |
| -----: | -------------------: | --------------------------------------: |
|    GET |            `/events` | List all events (sorted by start\_time) |
|   POST |            `/events` |                      Create a new event |
|    PUT | `/events/<event_id>` |                Update an existing event |
| DELETE | `/events/<event_id>` |                         Delete an event |


📌 Example event JSON
Use this JSON when creating or updating an event:

{
  "title": "Team meeting",
  "description": "Discuss project status",
  "start_time": "2025-07-01 10:00",
  "end_time": "2025-07-01 11:00"
}
