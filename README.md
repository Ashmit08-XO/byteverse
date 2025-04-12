# byteverse

Autonomous Ambulance Routing System
A real-time emergency ambulance routing system that helps locate the nearest and fastest hospital based on the user's current location, using Django REST Framework, React.js, Leaflet, and the OpenRouteService Matrix API.

📁 Project Structure
bash
Copy
Edit
ambulance_routing/
├── backend/
│   ├── hospitals/
│   │   ├── models.py
│   │   ├── serializers.py
│   │   ├── views.py               # Registration, login, and hospital APIs
│   │   ├── utils/
│   │   │   └── ors.py             # ORS API integration
│   │   └── routing/
│   │       ├── views.py           # Optimal hospital routing view
│   │       └── services.py        # Core logic to find nearest hospital
│   ├── ambulance_routing/
│   └── manage.py
├── frontend/
│   └── src/
│       ├── components/map/MapModal.jsx
│       ├── pages/login/Login.jsx
│       └── App.jsx
How to Run This Project Locally
🔁 Prerequisites
Python 3.10+

Node.js & npm

OpenRouteService API Key (get it here)

⚙️ Backend (Django + DRF)
bash
Copy
Edit
# Step 1: Go to the backend directory
cd backend

# Step 2: Create virtual environment
python -m venv env

# Step 3: Activate the environment
# On Windows:
env\Scripts\activate
# On Mac/Linux:
source env/bin/activate

# Step 4: Install Python dependencies
pip install -r requirements.txt

# Step 5: Run migrations
python manage.py makemigrations
python manage.py migrate

# Step 6: Start the backend server
python manage.py runserver
🛣️ Now the Django server is running at: http://localhost:8000

🌐 Frontend (React + Vite + Leaflet)
bash
Copy
Edit
# Step 1: Go to the frontend directory
cd frontend

# Step 2: Install Node dependencies
npm install axios 

# Step 3: Install Leaflet and Router
npm install react-leaflet leaflet react-router-dom

# Step 4: Start the React dev server
npm run dev
🌍 Open your app at: http://localhost:5173

✅ Make sure your backend is running before the frontend so the API calls succeed.



