From python:latest
ENV PORT 8080

COPY . /temp
WORKDIR /temp
# Install production dependencies.
RUN pip install --no-cache-dir -r requirements.txt

# Python WSGI HTTP Server
CMD exec gunicorn --bind :$PORT --workers 1 --threads 8 --timeout 0 hello:app
