
FROM python:3.8.12-slim

RUN apt-get update -y

RUN apt-get install tk -y
RUN pip install PILLOW
RUN pip install tensorflow && \
    pip install numpy \
    pip install keras --no-deps && \
    pip install pandas


ENV DISPLAY=host.docker.internal:0.0


copy ./python/Gui.py /app/Gui.py
Copy ./python/my_model.h5 /app/my_model.h5
Copy ./Test /app/Test
Copy ./Train /app/Train


Workdir /app


CMD ["Gui.py"]
ENTRYPOINT ["python3"]