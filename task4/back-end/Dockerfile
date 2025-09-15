# Utiliser Ubuntu le plus récent
FROM ubuntu:latest

# Mettre à jour le système
RUN apt-get update && apt-get upgrade -y

# Installer Python3 et pip3
RUN apt-get install -y python3 python3-pip

# Supprimer EXTERNALLY-MANAGED si nécessaire (erreur de pip)
RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED || true

# Installer Flask avec pip3
RUN pip3 install flask
RUN pip3 install flask-cors

# Créer un dossier de travail
WORKDIR /app

# Copier le fichier api.py dans le conteneur
COPY ./api.py /app/api.py

# Lancer le serveur Flask
CMD ["python3", "api.py"]
