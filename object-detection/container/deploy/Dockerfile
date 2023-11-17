FROM python:3.8

WORKDIR /app

COPY requirements.txt /app
RUN pip install -r requirements.txt
RUN pip install torch==1.12.1+cu113 torchvision==0.13.1+cu113 torchaudio==0.12.1 --extra-index-url https://download.pytorch.org/whl/cu113
COPY deploy.py /app
COPY common.py /app
COPY fasterrcnn_handler.py /app
# COPY index_to_name.json /app
COPY model-xview-template.py /app


ENV PYTHONUNBUFFERED=1
