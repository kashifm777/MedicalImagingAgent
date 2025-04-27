# 🩺 AI-Powered Medical Image Analysis Tool 🔬

This Streamlit application provides an AI-driven system for analyzing medical images (X-ray, MRI, CT, Ultrasound, etc.). Upload an image, and the tool will leverage a specialized AI agent powered by Google's Gemini model to provide detailed findings, a diagnostic assessment, a patient-friendly explanation, and relevant research context.

## ✨ Features

* **Medical Image Analysis:** Analyzes uploaded medical images (JPG, JPEG, PNG, BMP, GIF).
* **Detailed Report Generation:** Provides a structured report covering:
    * **Image Type & Region:** Identifies the imaging modality, anatomical region, positioning, and evaluates image quality.
    * **Key Findings:** Highlights primary observations, potential abnormalities with descriptions, and relevant measurements.
    * **Diagnostic Assessment:** Offers a primary diagnosis with a confidence level and a ranked list of differential diagnoses supported by evidence.
    * **Patient-Friendly Explanation:** Simplifies the findings into clear, non-technical language with analogies.
    * **Research Context:** Uses DuckDuckGo to find recent medical literature and standard treatment protocols, providing key references.
* **Powered by Gemini:** Utilizes the advanced capabilities of Google's `gemini-2.0-flash-exp` model for image analysis and report generation.
* **Web Search Integration:** Integrates DuckDuckGo for the AI agent to search for relevant medical literature and treatment protocols.
* **User-Friendly Interface:** A clean and intuitive Streamlit interface for easy image uploading and analysis.

## 🚀 App Demo

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://medical-image-analysis-ai.streamlit.app)

[https://medical-image-analysis-ai.streamlit.app](https://medical-image-analysis-ai.streamlit.app)

## ⚙️ Dependencies

* `streamlit`: For creating the web application interface.
* `Pillow (PIL)`: For image manipulation.
* `agno`: An AI agent framework for building intelligent agents.
* `python-dotenv`: For loading environment variables (like the Google API key).
* `google-generativeai`: The official Google Generative AI library.

You can install all the necessary dependencies using the `requirements.txt` file (if provided).

## 🔑 Setup

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/kashifm777/MedicalImagingAgent](https://github.com/kashifm777/MedicalImagingAgent)
    cd medical-image-analysis
    ```
2.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
3.  **Set up Google API Key:**
    * Ensure you have a Google Cloud Project with the Generative AI API enabled.
    * Obtain an API key for the Generative AI service.
    * Create a `.env` file in the project root and add your API key:
        ```dotenv
        GOOGLE_API_KEY=YOUR_GOOGLE_API_KEY
        ```
4.  **Run the Streamlit App:**
    ```bash
    streamlit run medical.py
    ```
5.  **Upload Image (Sidebar):**
    * In the sidebar, click on "Browse files" and upload your medical image.
6.  **Analyze Image:**
    * Click the "Analyze Image" button in the sidebar.
7.  **View Report:**
    * The AI-generated analysis report will be displayed on the main screen, covering the image type, findings, diagnostic assessment, patient-friendly explanation, and research context.

## 🧠 How It Works

This application utilizes the `agno` library to create a specialized `medical_agent` powered by Google's Gemini model. When you upload an image and click "Analyze Image," the following steps occur:

1.  **Image Loading and Preprocessing:** The uploaded image is loaded using Pillow (PIL) and resized to a standard width for efficient processing.
2.  **AI Agent Execution:** The resized image, along with a detailed prompt outlining the desired analysis structure, is passed to the `medical_agent`.
3.  **Multi-faceted Analysis:** The Gemini model, guided by the prompt and potentially leveraging the DuckDuckGo tool for research, analyzes the image and generates a comprehensive report covering the specified sections.
4.  **Structured Output:** The generated report, formatted in Markdown, is displayed in the Streamlit application.

## ➕ Further Enhancements

* Support for DICOM files.
* Integration with medical image viewers.
* Options for users to provide additional clinical context.
* Visual highlighting of key findings on the uploaded image.
* Saving and sharing analysis reports.

## 🙏 Contributing

Contributions to this project are welcome! Feel free to submit pull requests with bug fixes, new features, or improvements.

## 📄 License

[Your License Here (e.g., MIT License)](LICENSE)