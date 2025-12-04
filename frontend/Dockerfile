FROM python:3.10

# Create app directory
WORKDIR /app

# Install pip dependencies
RUN pip install --no-cache-dir \
    streamlit \
    requests

# Copy your frontend code
COPY . .

# Expose Streamlit port
EXPOSE 8501

# Set default backend/API URL
# (You override this at runtime)
ENV API_URL=""

# Run the Streamlit app
CMD ["streamlit", "run", "app.py", "--server.port=8501", "--server.address=0.0.0.0"]
