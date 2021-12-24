
# Slim version of Python
FROM python:3.8.12-slim

# Download Package Information
RUN apt-get update -y

# Install Tkinter
RUN apt-get install tk -y
RUN pip install PILLOW
RUN pip install tensorflow && \
    pip install numpy \
    pip install keras --no-deps && \
    pip install pandas

ENV DISPLAY=host.docker.internal:0.0

copy ./traffic_signs.py /app/traffic_signs.py
Copy ./my_model.h5 /app/my_model.h5
Copy ./Test /app/Test
Copy ./Train /app/Train
Workdir /app
# Commands to run Tkinter application
CMD ["traffic_signs.py"]
ENTRYPOINT ["python3"]