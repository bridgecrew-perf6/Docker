FROM python:3.8

RUN apt-get update && apt-get install -y git && \
    rm -rf /var/lib/apt/lists/*

RUN git clone https://github.com/ilya-shanin/VCCPlanning /app && \
    mv /app/V3C/urls.py /app/V3C/urls.back

WORKDIR /app

RUN rm -rf accounts/migrations && \
    rm -rf events/migrations && \
    rm -rf participants/migrations

COPY . /app/

RUN pip install --upgrade pip && \
    pip install -r requirements.txt

EXPOSE 80