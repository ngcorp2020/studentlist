FROM python:3.10-slim

RUN apt-get update && apt-get install -y \
    build-essential\
    gcc\
    python3-dev\
    libsasl2-dev \
    libldap2-dev \
    libssl-dev \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY student_age.py .
COPY student_age.json /data/student_age.json

ENV student_age_file_path=/data/student_age.json

EXPOSE 5000

CMD ["python", "student_age.py"]

