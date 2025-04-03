FROM python:3.10-slim

RUN apt-get update && \
    apt-get install -y tesseract-ocr poppler-utils libgl1-mesa-glx && \
    apt-get clean && \
    pip install --no-cache-dir streamlit pytesseract opencv-python-headless pdf2image reportlab boto3 python-dotenv sqlite-utils paramiko

WORKDIR /app
COPY . /app

EXPOSE 8501
CMD ["streamlit", "run", "ui/app.py"]
