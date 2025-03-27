# Catalyst_hackathon

# EduMentor AI

EduMentor AI is an AI-powered educational platform built with Streamlit, designed to assist students through an interactive, text-based interface. Leveraging natural language processing (NLP) with the LLaMA 3 model, it offers personalized study help, note generation, quizzes, and learning games. Hosted on Streamlit Community Cloud, EduMentor AI aims to make learning engaging and accessible.

## Features

- **Text-Based Q&A:** Ask questions via a chat interface and receive detailed, AI-generated responses.
- **Note Generation:** Automatically summarizes input into concise, study-ready notes.
- **Quiz Creation:** Generates custom quizzes based on user-specified topics.
- **Learning Games:** Interactive challenges to test knowledge and enhance engagement.

> **Note:** Voice input is planned but not yet implemented due to deployment constraints.

## Tech Stack

### **Frontend:**
- **Streamlit (>=1.44.0)** – Rapid web app development.

### **Backend:**
- **LangChain (>=0.3.21) & LangChain Community (>=0.3.20)** – NLP framework.
- **Ollama (>=0.4.7)** – Interface to LLaMA 3 model.

### **Deployment:**
- **Streamlit Community Cloud** – Free hosting platform.

## Project Structure

```bash
EduMentor-AI/
├── app.py              # Main Streamlit app
├── requirements.txt    # Python dependencies
├── src/
│   ├── components/
│   │   ├── conversation.py  # AI conversation logic
│   │   ├── sidebar.py       # Navigation UI
│   │   └── voice_input.py   # Text input handling (voice planned)
└── README.md           # This file
```

## Installation

### **Prerequisites**
- Python 3.11 or 3.12
- Git
- Ollama installed locally

### **Steps**

#### **Clone the Repository:**
```bash
git clone https://github.com/your-username/EduMentor-AI.git
cd EduMentor-AI
```

#### **Set Up Virtual Environment:**
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
```

#### **Install Dependencies:**
```bash
pip install -r requirements.txt
```

#### **Run Ollama Server:**
```bash
ollama serve
```

#### **In a separate terminal:**
```bash
ollama pull llama3
```

#### **Launch the App:**
```bash
streamlit run app.py
```

Open your browser to [http://localhost:8501](http://localhost:8501).

## Deployment

EduMentor AI is deployed on Streamlit Community Cloud:

1. Push the repository to GitHub.
2. Connect it to Streamlit Cloud via the dashboard.
3. The app auto-deploys with `requirements.txt`.

> **Note:** Audio features (`streamlit-mic-recorder`, `speechrecognition`, `pyaudio`) were excluded from deployment due to Streamlit Cloud’s lack of system dependency support (e.g., `portaudio19-dev`).

## Challenges

### **Audio Integration**
- Planned voice input with PyAudio failed on Streamlit Cloud due to missing `portaudio.h`.
- **Solution:** Focused on a text-only version for deployment compatibility.

## Future Enhancements

- **Voice Input:** Add browser-based audio recording with `streamlit-mic-recorder` and external speech-to-text (e.g., Google Speech-to-Text).
- **Offline Speech:** Integrate a local model (e.g., Whisper) on a platform like Heroku.
- **Multi-Language:** Support additional languages via LLaMA 3.
- **Mobile UI:** Optimize for mobile devices.
- **Game Expansion:** Add scoring and leaderboards.

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a feature branch:
   ```bash
   git checkout -b feature-name
   ```
3. Commit changes:
   ```bash
   git commit -m "Add feature"
   ```
4. Push to your fork:
   ```bash
   git push origin feature-name
   ```
5. Open a pull request.

## License

This project is licensed under the MIT License – see the `LICENSE` file for details.

## Acknowledgments

Built with ❤️ for educational innovation.

Thanks to Streamlit, LangChain, and Ollama communities.
