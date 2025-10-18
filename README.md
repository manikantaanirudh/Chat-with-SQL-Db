# 🦜 LangChain Chat with SQL Database

A powerful Streamlit application that allows you to chat with your SQL database using natural language queries powered by LangChain and Groq AI.

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Streamlit](https://img.shields.io/badge/Streamlit-1.44+-red.svg)
![LangChain](https://img.shields.io/badge/LangChain-0.3+-green.svg)
![Groq](https://img.shields.io/badge/Groq-AI-orange.svg)

## 🌟 Features

- **🗣️ Natural Language Queries**: Ask questions about your database in plain English
- **🤖 AI-Powered SQL Generation**: Automatically converts your questions to SQL queries
- **📊 Multiple Database Support**: Works with SQLite and MySQL databases
- **⚡ Real-time Responses**: Get instant answers from your database
- **🎨 Beautiful UI**: Clean and intuitive Streamlit interface
- **🔄 Error Handling**: Robust error handling with parsing error recovery
- **📱 Responsive Design**: Works on desktop and mobile devices

## 🚀 Quick Start

### Prerequisites

- Python 3.8 or higher
- Groq API key ([Get one here](https://console.groq.com/))

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/manikantaanirudh/Chat-with-SQL-Db.git
   cd Chat-with-SQL-Db
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the application**
   ```bash
   streamlit run app.py
   ```

4. **Open your browser**
   - Navigate to `http://localhost:8501`
   - Enter your Groq API key in the sidebar
   - Start chatting with your database!

## 📋 Sample Data

The application comes with a pre-loaded SQLite database containing student information:

| Name   | Class       | Section | Marks |
|--------|-------------|---------|-------|
| Krish  | Data Science| A       | 90    |
| John   | Data Science| B       | 100   |
| Mukesh | Data Science| A       | 86    |
| Jacob  | DEVOPS      | A       | 50    |
| Dipesh | DEVOPS      | A       | 35    |

## 💬 Example Queries

Try asking these questions to see the AI in action:

- "Show me all student names"
- "Who has the highest marks?"
- "What's the average marks for Data Science students?"
- "How many students are in section A?"
- "List all students with marks above 80"
- "Which class has the most students?"

## 🛠️ Configuration

### Database Options

The application supports two database configurations:

1. **SQLite (Default)**
   - Uses the included `student.db` file
   - No additional setup required

2. **MySQL**
   - Select "Connect to your MySQL Database" in the sidebar
   - Provide MySQL connection details:
     - Host
     - Username
     - Password
     - Database name

### AI Model

The application uses Groq's `llama-3.1-8b-instant` model for fast and accurate responses. You can modify the model in `app.py`:

```python
llm=ChatGroq(groq_api_key=api_key,model_name="llama-3.1-8b-instant",streaming=True)
```

**Available Models:**
- `llama-3.1-8b-instant` (fast, good for most queries)
- `llama-3.1-70b-versatile` (more powerful, slower)
- `mixtral-8x7b-32768` (balanced performance)

## 📁 Project Structure

```
Chat-with-SQL-Db/
├── app.py              # Main Streamlit application
├── sqlite.py           # Database setup script
├── student.db          # Sample SQLite database
├── requirements.txt    # Python dependencies
├── .gitignore         # Git ignore file
└── README.md          # This file
```

## 🔧 Technical Details

### Architecture

- **Frontend**: Streamlit for the web interface
- **AI Engine**: LangChain for natural language processing
- **LLM Provider**: Groq for fast AI responses
- **Database**: SQLite (default) or MySQL support
- **SQL Generation**: LangChain SQL Agent with error handling

### Key Components

1. **SQL Agent**: Converts natural language to SQL queries
2. **Database Toolkit**: Provides database interaction tools
3. **Streamlit Callbacks**: Real-time response streaming
4. **Error Handling**: Robust parsing error recovery

## 🚨 Troubleshooting

### Common Issues

1. **Model Error**: If you get a model decommissioned error, update the model name in `app.py`
2. **API Key Error**: Make sure your Groq API key is valid and has sufficient credits
3. **Database Connection**: Ensure the database file exists and is accessible
4. **Port Already in Use**: If port 8501 is busy, Streamlit will automatically use the next available port

### Error Messages

- **"File does not exist: app.py"**: Make sure you're in the correct directory
- **"Parsing LLM output error"**: The application includes error handling for this
- **"Model decommissioned"**: Update to a supported model name

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- [LangChain](https://github.com/langchain-ai/langchain) for the powerful AI framework
- [Streamlit](https://streamlit.io/) for the amazing web framework
- [Groq](https://groq.com/) for the fast AI inference
- [SQLAlchemy](https://www.sqlalchemy.org/) for database abstraction

## 📞 Support

If you have any questions or need help, please:

1. Check the [Issues](https://github.com/manikantaanirudh/Chat-with-SQL-Db/issues) page
2. Create a new issue if your problem isn't already reported
3. Provide detailed information about your setup and the error

## 🌟 Star the Repository

If you found this project helpful, please give it a star ⭐ on GitHub!

---

**Made with ❤️ using LangChain, Streamlit, and Groq AI**
