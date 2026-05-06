FROM python:3.11

WORKDIR /app

COPY requirements.txt .

RUN pip install --upgrade pip

RUN pip install --default-timeout=1000 --no-cache-dir -r requirements.txt

# Install Torch separately (CPU optimized)
RUN pip install torch==2.1.0 --index-url https://download.pytorch.org/whl/cpu

COPY . .

EXPOSE 8000

CMD ["python", "run.py"]