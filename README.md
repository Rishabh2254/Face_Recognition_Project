# Face_Recognition_Project
Hi, My name is Rishabh Srivastava. This is a Face Recognition Project that i made.


Face Recognition System
A secure and efficient face recognition system built using Flask and PostgreSQL for registration and authentication through facial recognition.

Features
User Registration: Capture and store user face embeddings during registration.
Login Authentication: Authenticate users by comparing live face data with stored embeddings.
Secure Database: PostgreSQL database to store user credentials and embeddings.
Real-Time Face Detection: Utilizes the webcam for real-time face capture.
Installation
Prerequisites
Python 3.8 or above
PostgreSQL
Virtual Environment (optional but recommended)
Steps
Clone this repository:

bash
Copy code
git clone https://github.com/your-username/face-recognition-system.git
cd face-recognition-system
Set up a virtual environment (optional):

bash
Copy code
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
Install dependencies:

bash
Copy code
pip install -r requirements.txt
Configure PostgreSQL:

Create a PostgreSQL database named face_recognition_db.
Update the SQLALCHEMY_DATABASE_URI in app/__init__.py with your PostgreSQL credentials.
Set up the database:

bash
Copy code
flask shell
>>> from app import db
>>> db.create_all()
>>> exit()
Run the application:

bash
Copy code
flask run
Open the application in your browser:

arduino
Copy code
http://127.0.0.1:5000/
Project Structure
csharp
Copy code
face-recognition-system/
├── app/
│   ├── __init__.py       # Flask application factory
│   ├── models.py         # Database models
│   ├── routes.py         # Application routes
│   ├── face_recognition.py # Face recognition logic
│   ├── static/           # Static files (CSS, JS)
│   ├── templates/        # HTML templates
├── migrations/           # Database migrations (if applicable)
├── README.md             # Project documentation
├── requirements.txt      # Python dependencies
Usage
Register:

Navigate to the /register page.
Enter your username and capture your face via the webcam.
Once the face is successfully captured, the user is registered.
Login:

Navigate to the /login page.
Capture your face for authentication.
If matched, you will be authenticated and redirected.
Dependencies
Flask
Flask-SQLAlchemy
OpenCV
PostgreSQL
Face recognition libraries (e.g., dlib, face_recognition)
Known Issues
Ensure the webcam is functional and permissions are granted.
Face recognition may not work optimally under poor lighting conditions.
Contributing
Contributions are welcome! Please follow these steps:

Fork the repository.
Create a feature branch:
bash
Copy code
git checkout -b feature-name
Commit your changes:
bash
Copy code
git commit -m "Add feature description"
Push to the branch:
bash
Copy code
git push origin feature-name
Open a pull request.
