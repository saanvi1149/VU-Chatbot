VURA – AI Chatbot for Vidyashilp University
VURA is an AI-powered chatbot built using Retrieval-Augmented Generation (RAG) architecture. It integrates ChromaDB (vector database) and Google Gemini API (LLM) to provide accurate, real-time responses for university-related queries such as attendance, timetable, and general information.

The system supports multilingual interaction, voice input/output, and intelligent query handling.
Features
-AI-powered question answering (RAG-based)

- Attendance access for students and faculty

-Timetable and schedule retrieval

-Multilingual support (English, Hindi, Kannada, etc.)

-Voice input (speech-to-text) and output (text-to-speech)

-Email fallback system for unanswered queries

-Smart query normalization (basic typo handling)
 Architecture
User Input
↓
FastAPI Backend
↓
Language Detection + Translation
↓
Query Normalization
↓
RAG Pipeline
↓
ChromaDB (Vector Search)
↓
Gemini API (LLM)
↓
Final Response (Text + Voice)

Tech Stack
-Backend: Python, FastAPI

-Database: ChromaDB (Vector DB)

-LLM: Google Gemini API (gemini-2.5-flash)

-Embeddings: HuggingFace (all-mpnet-base-v2)

-Data Processing: Pandas

-Translation: Deep Translator

-Voice: SpeechRecognition, gTTS

Workflow
1.User enters query (text or voice)

2.Language is detected automatically

3.Query is translated to English (for retrieval)

4.Query is normalized (spelling corrections)

5.Relevant chunks retrieved from ChromaDB

6.Gemini generates a detailed response

7.Response returned in user’s language

8.Optional: voice output generated

How to Run the Project
1️. Clone the repository
git clone https://github.com/your-username/vura-chatbot.git
cd vura-chatbot

2️. Install dependencies
pip install -r requirements.txt

3️. Set up API Key
Create a .env file inside backend folder:
API_KEY=your_gemini_api_key_here

4️. Prepare Data
Add all .txt files inside:
/backend/data/

5️. Build ChromaDB
python database.py

6️. Run Backend
uvicorn main:app --reload

7️. Test RAG
python rag.py

Limitations
-Sensitive to spelling mistakes (limited correction rules)

-No conversational memory (each query is independent)

-Depends entirely on provided dataset

-Fixed chunking may split important information

-Retrieval accuracy may vary (no re-ranking)

-Multilingual support depends on translation quality

-API dependency (Gemini may have downtime or rate limits)

Future Scope
-Add advanced spell correction (AI-based)

-Implement conversational memory (chat history)

-Improve retrieval using re-ranking models

-Deploy as web/mobile application

-Integrate with live university databases

-Add authentication with real-time student systems

Team Contribution
Rithunya Satish	-	LLM , Prompt Engineering, Backend & RAG Engine
Saanvi V	-	LLM , Prompt Engineering, Backend & RAG Engine
Dishitha Ramesh	-	Data Scraping	
Chaithra M	-	(Frontend)  Website UI	
Keshav Sai Kudum	-	(Frontend) Chatbot System	
SK Doddana Gouda	-	Report, PPT 

Impact of the Solution
-Reduces dependency on manual university support

-Provides instant responses to student queries

-Improves accessibility through multilingual support

-Enhances user experience using AI automation

 Conclusion
    VURA demonstrates how Retrieval-Augmented Generation (RAG) combined with modern LLMs can be used to build intelligent and scalable chatbot systems for educational institutions.



Tags
AI, Chatbot, RAG, ChromaDB, FastAPI, LLM, Gemini, NLP
