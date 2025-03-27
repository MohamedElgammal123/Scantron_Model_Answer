Scantron Highlighter App
This Streamlit web application highlights correct answers on a Scantron sheet image and optionally overlays the exam model code (e.g., 00, 11, ..., 99). The app uses uploaded Excel files that contain the correct answers and lets you choose the exam model to generate a visual reference.

🚀 Features
Upload an Excel file with correct answers

Choose an exam model code (00–99)

Visualize highlighted answers and exam code on the Scantron image

Download the highlighted Scantron as a JPG

View a table of the correct answers

📁 Project Structure
bash
Copy
Edit
├── app.py                  # Main Streamlit app
├── coordinates.xlsx        # Coordinates for answer bubbles and exam codes
├── Scantron Sheet.jpg      # Base image of the Scantron sheet
├── requirements.txt        # Python dependencies
└── README.md               # You're reading it now
📝 Input File Format
Upload an Excel file with the following columns:

Question	Answer
1	A
2	C
...	...
✅ Usage
Clone this repo or copy the files to your working directory.

Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt
Run the app:

bash
Copy
Edit
streamlit run app.py
Upload the answer key Excel file.

Select the exam model code from the dropdown.

Click "Generate Model Answer" to visualize and download the result.

📦 Requirements
Python 3.7+

streamlit

pandas

matplotlib

openpyxl

📌 Notes
Make sure coordinates.xlsx contains two sheets:

Sheet1: Contains bubble coordinates with columns: Question, Answer, X, Y

Sheet2: Contains model code positions with columns: code, x1, y1, x2, y2

🖼️ Output
A high-resolution JPG of the Scantron sheet with:

Correct answer bubbles marked in black

Exam model code highlighted

