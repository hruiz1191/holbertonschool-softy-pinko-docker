FROM ubuntu:latest

WORKDIR /app

# Instala Python3, pip3, y quita restricción de paquetes externos
RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y python3 python3-pip && \
    rm -f /usr/lib/python*/EXTERNALLY-MANAGED

# Instala Flask con pip3
RUN pip3 install flask

RUN pip3 install flask-cors

# Copia el archivo Python
COPY ./api.py /app/api.py

# Expone el puerto 5252
EXPOSE 5252

# Ejecuta el servidor Flask
CMD ["python3", "api.py"]
