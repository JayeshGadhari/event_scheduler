# 🗓️ Event Scheduler API

A simple Python + Flask REST API to **create, list, update, and delete calendar events**.  
Great as a small backend project or for learning REST APIs, JSON storage & Postman testing.

---

## 🚀 Getting started

Follow these steps to run the project locally:

1️⃣ Clone this repository or download & unzip it.

2️⃣ Install dependencies:
```bash
pip install -r requirements.txt
```

3️⃣ Make sure the `events.json` file exists and contains at least:
```json
[]
```

4️⃣ Start the Flask server:
```bash
python app.py
```

API will be running at:
```
http://127.0.0.1:5000
```

---

## 📦 Project structure

```
event_scheduler/
├── app.py                                  # Main Flask app with API endpoints
├── storage.py                              # Helpers to load/save events to JSON
├── events.json                             # JSON file to store events
├── requirements.txt                        # Python dependencies
├── README.md                               # Project documentation
└── Event Scheduler.postman_collection.json # Postman collection to test API
```

---

## 🧪 How to test with Postman

No need to build frontend — just use Postman:

1️⃣ Open Postman → click **Import**

2️⃣ Select:
```
Event Scheduler.postman_collection.json
```

3️⃣ Use the saved requests:

| Method | Endpoint                | Purpose                          |
|------:|------------------------:|---------------------------------:|
| GET   | `/events`               | List all events (sorted by start time) |
| POST  | `/events`               | Create a new event |
| PUT   | `/events/<event_id>`    | Update an existing event |
| DELETE| `/events/<event_id>`    | Delete an event |

✅ Each request already includes sample JSON body.

---

## 📌 Example JSON for creating/updating event

```json
{
  "title": "Team meeting",
  "description": "Discuss project updates",
  "start_time": "2025-07-01 10:00",
  "end_time": "2025-07-01 11:00"
}
```

---

## ✅ Features

- Add events (auto-generated unique IDs)
- List events sorted by start time
- Update event details by ID
- Delete events by ID
- Simple JSON storage (easy to view & edit)

---
---

## 🧰 Quick code overview

- `app.py`  
  - `/events` → `GET` list & `POST` create
  - `/events/<event_id>` → `PUT` update & `DELETE` delete
- `storage.py`  
  - `load_events()` → read events from `events.json`
  - `save_events(events)` → write events to `events.json`
- `events.json` → starts with `[]`, grows as you add events.

---

## 📌 Requirements

- Python 3.7+
- Flask (installed via requirements.txt)

---
