# GLR Pipeline - Insurance Template Automation

Automate insurance template filling using photo reports and AI via Streamlit.

## Features

- Upload insurance templates (.docx format)
- Upload multiple photo reports (.pdf format)
- Extract text from PDFs automatically
- Use AI (Llama 3.3 70B via Groq) to interpret and map data
- Generate filled-in Word documents
- Download as DOCX or PDF (with LibreOffice installed)

## Setup

### Local Development

1. Install dependencies:
```bash
pip install -r requirements.txt
```

2. Create a `.env` file with your Groq API key:
```
GROQ_API_KEY=your_groq_api_key_here
```

3. (Optional) Install LibreOffice for PDF conversion:
   - Download from: https://www.libreoffice.org/download/download/
   - Install and restart your terminal

4. Run the app:
```bash
streamlit run app.py
```

### Deployment to Streamlit Cloud

1. Push your code to GitHub
2. Connect to Streamlit Cloud
3. Add your `GROQ_API_KEY` in Secrets (Settings > Secrets):
```toml
GROQ_API_KEY = "your_groq_api_key_here"
```
4. The `packages.txt` file will automatically install LibreOffice for PDF conversion

## Usage

1. Upload your insurance template (.docx) - ONE file
2. Upload one or more photo reports (.pdf) - ONE or MORE files
3. Click "Process Documents"
4. Download the completed report as DOCX or PDF

## How It Works

1. **Text Extraction**: Extracts text from PDF photo reports using PyPDF2
2. **Template Analysis**: Reads the Word template structure
3. **AI Processing**: Sends template and report data to Llama 3.3 70B via Groq
4. **Data Mapping**: AI identifies key-value pairs and creates mappings
5. **Template Filling**: Populates the template with extracted data (preserves formatting)
6. **Output Generation**: Creates downloadable .docx and .pdf files

## API Configuration

The app uses Groq's free Llama 3.3 70B model. Get your free API key at [console.groq.com](https://console.groq.com)

## PDF Conversion

- **With LibreOffice**: Full formatting preservation, works on all platforms
- **Without LibreOffice**: DOCX download only (users can convert manually)
- **Streamlit Cloud**: Automatically installs LibreOffice via `packages.txt`
