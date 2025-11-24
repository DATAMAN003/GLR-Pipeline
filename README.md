# GLR Pipeline - Insurance Template Automation

🚀 **Live App:** https://dataman003.streamlit.app/

Automate insurance template filling using photo reports and AI. No API key required - just upload your files and get results!

## ✨ Features

- 📄 Upload insurance templates (.docx format)
- 📸 Upload multiple photo reports (.pdf format)
- 🤖 AI-powered data extraction using Llama 3.3 70B
- 📝 Automatic template filling with formatting preservation
- ⬇️ Download completed reports instantly
- 🔒 No API key needed for users

## 🎯 How to Use

1. **Visit the app:** https://dataman003.streamlit.app/
2. **Upload your template** - ONE .docx file
3. **Upload photo reports** - ONE or MORE .pdf files
4. **Click "Process Documents"**
5. **Download your completed report**

That's it! No setup, no API keys, no technical knowledge required.

## 🛠️ For Developers

### Local Development

1. Clone the repository:
```bash
git clone https://github.com/DATAMAN003/GLR-Pipeline.git
cd GLR-Pipeline
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Create a `.streamlit/secrets.toml` file with your Groq API key:
```toml
GROQ_API_KEY = "your_groq_api_key_here"
```

4. Run the app:
```bash
streamlit run app.py
```

### Deployment to Streamlit Cloud

1. Fork this repository
2. Connect to Streamlit Cloud
3. Add your `GROQ_API_KEY` in app settings (Settings > Secrets):
```toml
GROQ_API_KEY = "your_groq_api_key_here"
```
4. Deploy! The `packages.txt` file will automatically install LibreOffice

## 🔧 How It Works

1. **Template Analysis** - AI learns the structure and formatting of your template
2. **Text Extraction** - Extracts all text from PDF photo reports
3. **AI Processing** - Llama 3.3 70B analyzes and maps data intelligently
4. **Smart Filling** - Populates template while preserving all formatting
5. **Output Generation** - Creates professional Word documents ready to download

## 🎨 Technology Stack

- **Frontend:** Streamlit
- **AI Model:** Llama 3.3 70B (via Groq)
- **Document Processing:** python-docx, PyPDF2
- **PDF Conversion:** LibreOffice (server-side)

## 📝 License

MIT License - feel free to use and modify!

## 🤝 Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

## 📧 Contact

For questions or support, please open an issue on GitHub.
