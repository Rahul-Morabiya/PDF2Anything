# PDF2Anything
PDF2Anything_Mined_Hackathon_Team_GodLevel

![image](https://github.com/user-attachments/assets/6563200c-e258-450c-b73a-ba8aa45f06a1)


# Academic Research Remix by Cactus Communications

**Convert academic research papers into engaging multi-format content!**

This project is part of the hackathon track **"Academic Research Remix By Cactus Communications."** It transforms academic research papers into alternative content formats such as:
- **Podcast** (short form, long form, multilingual, human-like audio conversation)
- **PowerPoint Presentations** (formal conference-style or fun explainer for a wider audience)
- **Analysis Reports** (summaries, thorough analysis, citations, literature reviews, rejection checkers)

The application leverages:
- **Google Gemini API** for generating content from the research paper text.
- **Google Cloud Text-to-Speech (TTS)** for converting text (e.g., podcast scripts) to audio.
- **PyMuPDF** for extracting text from PDF files.
- **python-pptx** for creating PowerPoint presentations.
- **Flask** as the web framework and **Flask-CORS** for cross-origin resource sharing.

---

## Features

- **PDF Upload & Text Extraction:** Upload research papers in PDF format and extract text.
- **Podcast Generation:** Create conversational scripts using AI, then synthesize human-like audio.
- **PPT Generation:** Generate PowerPoint presentations with customizable themes and slide counts.
- **Research Analysis:** Use AI to generate different types of research analysis such as summaries, detailed reviews, or citation extraction.
- **Responsive Web Interface:** A user-friendly front end with theme switching and interactive forms.

---

## Prerequisites

Make sure you have the following installed on your system:

- Python 3.7 or higher
- pip (Python package installer)
- [Google Cloud TTS Service Account JSON](https://cloud.google.com/text-to-speech/docs/reference/libraries) with necessary permissions
- API key for [Google Gemini API](https://developers.generativelanguage.google)

---

![image](https://github.com/user-attachments/assets/6f66268d-c6d3-427b-ac1a-39d87be72bef)


![image](https://github.com/user-attachments/assets/55312b6a-b0ff-495d-9ef5-97d052efd5d5)


## Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/yourusername/academic-research-remix.git
    cd academic-research-remix
    ```

2. **(Optional) Create and activate a virtual environment:**

    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```

3. **Install required packages:**

    Create a `requirements.txt` file with the following dependencies:

    ```plaintext
    Flask
    flask-cors
    google-cloud-texttospeech
    requests
    PyMuPDF
    python-pptx
    ```

    Then run:

    ```bash
    pip install -r requirements.txt
    ```

---

## Configuration

1. **Environment Variables:**

   Set up your environment variables for API keys and configuration:

    - **GEMINI_API_KEY:** Your Gemini API key.
    - **GOOGLE_CLOUD_TTS_KEY_PATH:** The file path to your Google Cloud TTS service account JSON file.

   You can set these in your shell before running the application, for example:

    ```bash
    export GEMINI_API_KEY="your_gemini_api_key_here"
    export GOOGLE_CLOUD_TTS_KEY_PATH="/path/to/your/service_account.json"
    ```

   Alternatively, update the corresponding variables in the code if you're testing locally (remember to remove or secure them for production).

2. **Directory Structure:**

   The application will automatically create the following directories if they do not exist:
   - `uploads` – for uploaded PDF files.
   - `static` – for generated audio files.
   - `conversations` – for saved podcast scripts.
   - `ppt` – for generated PowerPoint presentations.
   - `analysis` – for analysis result files.

---

## Running the Application

To start the Flask server in development mode, run:

```bash
python app.py
The server will be available at http://localhost:5000.

Usage
Navigate to the Home Page:

Open your browser and go to http://localhost:5000.

Upload a Research Paper:

Use the provided forms on the home page to upload a PDF.
Select your desired output format (Podcast, PPT, or Analysis) and configure options like audience, tone, or slide count.
Submit the form to generate the content.
Download the Output:

Once processing is complete, download links will be provided to access the generated podcast audio, conversation script, PowerPoint file, or analysis text.

