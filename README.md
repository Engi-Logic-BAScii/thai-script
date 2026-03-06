# Thai Consonant Drill - Project Template

A full-stack web application template for students, featuring a **Thai language learning tool** with a frontend-backend architecture. Use this as a starting point for your own projects!

## 📚 About This Template

This template demonstrates a complete, production-ready web application structure with:
- **Frontend**: Interactive HTML/CSS/JavaScript web interface
- **Backend**: FastAPI REST API with database integration
- **Database**: PostgreSQL with SQLAlchemy ORM
- **Architecture**: Separated frontend and backend with CORS for secure communication

> **For Students**: This template shows you how to build a real-world application. You can replace the Thai consonant drill logic with your own project ideas!

---

## 🚀 Quick Start

### Prerequisites
- **Python 3.8+** installed
- **PostgreSQL** installed and running
- Basic understanding of Python and web concepts

### Installation

1. **Clone the repository** (or use this as a template)
   ```bash
   git clone <repository-url>
   cd thai-script
   ```

2. **Set up the backend**
   ```bash
   cd backend
   pip install -r requirements.txt
   ```

3. **Configure the database**
   - Create a PostgreSQL database:
     ```bash
     createdb thai_script_db
     ```
   - Update the database URL in `backend/app/database.py` if needed

4. **Run the backend server**
   ```bash
   uvicorn app.main:app --reload
   ```
   - Server runs at `http://localhost:8000`
   - API docs available at `http://localhost:8000/docs`

5. **Open the frontend**
   - Open `index.html` in your browser (or use a local server)
   - Frontend connects to the backend API automatically

---

## 📁 Project Structure

```
thai-script/
├── index.html              # Frontend user interface
├── README.md              # This file
└── backend/
    ├── requirements.txt    # Python dependencies
    └── app/
        ├── main.py        # FastAPI application & routes
        ├── database.py    # Database configuration & connection
        ├── models.py      # SQLAlchemy database models
        └── schemas.py     # Pydantic request/response schemas
```

### Key Files Explained

| File | Purpose |
|------|---------|
| `index.html` | Frontend UI - displays the quiz interface |
| `main.py` | API endpoints - handles requests from frontend |
| `database.py` | Database setup - creates tables and connections |
| `models.py` | Data models - defines what gets stored in the database |
| `schemas.py` | Request/response schemas - validates API data |

---

## 🛠️ How to Customize for Your Project

### 1. **Change the Project Name**
   - Update the title in `index.html`
   - Update the app title in `main.py`: `FastAPI(title="Your Project Name")`
   - Rename the database in `database.py` and PostgreSQL

### 2. **Modify the Database Schema**
   - Edit `backend/app/models.py` to define your data:
     ```python
     class YourModel(Base):
         __tablename__ = "your_table"
         id = Column(Integer, primary_key=True)
         # Add your fields here
     ```
   - Update schemas in `schemas.py` accordingly

### 3. **Create New API Endpoints**
   - Add routes in `backend/app/main.py`:
     ```python
     @app.get("/api/your-endpoint")
     def your_endpoint(db: Session = Depends(get_db)):
         # Your logic here
         return {"data": "result"}
     ```

### 4. **Update the Frontend**
   - Modify `index.html` to match your interface
   - Update API calls to use your new endpoints

---

## 📡 API Documentation

Once the backend is running, visit **http://localhost:8000/docs** to see interactive API documentation (Swagger UI).

### Example Endpoints (from this template)
- `POST /api/quiz/start` - Start a quiz session
- `POST /api/quiz/answer` - Submit an answer
- And more...

---

## 🔧 Technology Stack

- **Frontend**: HTML5, CSS3, JavaScript (vanilla)
- **Backend**: FastAPI (Python web framework)
- **Database**: PostgreSQL + SQLAlchemy ORM
- **Server**: Uvicorn (ASGI server)

### Dependencies (`requirements.txt`)
```
fastapi          # Web framework
uvicorn         # ASGI server
sqlalchemy      # ORM for database
psycopg2-binary # PostgreSQL driver
python-dotenv   # Environment variables
pydantic        # Data validation
```

---

## 💡 Learning Objectives

By using this template, you'll learn:
- ✅ How to structure a full-stack web application
- ✅ How to build a REST API with FastAPI
- ✅ How to connect frontend to backend
- ✅ How to use databases with an ORM
- ✅ How to validate data with Pydantic schemas
- ✅ How to enable CORS for secure cross-origin requests

---

## 🐛 Troubleshooting

### Backend won't start
- Check if PostgreSQL is running
- Verify database credentials in `database.py`
- Install all requirements: `pip install -r requirements.txt`

### Frontend can't connect to backend
- Ensure backend is running on `http://localhost:8000`
- Check browser console (F12) for error messages
- Verify CORS is enabled in `main.py`

### Database errors
- Check PostgreSQL is installed and running
- Ensure the database exists: `createdb thai_script_db`
- Check SQLAlchemy models match the database schema

---

## 📝 Tips for Students

1. **Read the code** - Understand how each file works before modifying
2. **Use the API docs** - Test endpoints at `/docs` before calling from frontend
3. **Start small** - Make one change at a time and test it
4. **Ask for help** - When stuck, check error messages and use them as clues
5. **Experiment** - This is a template for learning, so don't be afraid to break things!

---

## 📚 Additional Resources

- [FastAPI Documentation](https://fastapi.tiangolo.com/)
- [SQLAlchemy Tutorial](https://docs.sqlalchemy.org/)
- [PostgreSQL Docs](https://www.postgresql.org/docs/)
- [MDN Web Docs](https://developer.mozilla.org/) - Frontend resources

---

## ✨ Next Steps

1. Clone or fork this repository
2. Follow the Quick Start section
3. Customize for your project
4. Add your own database models and API routes
5. Build your frontend interface
6. Deploy to the cloud (Heroku, AWS, etc.)

---

**Happy coding! 🚀**