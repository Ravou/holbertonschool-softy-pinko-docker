FROM ubuntu:latest

# Mise à jour et upgrade
RUN apt-get update && apt-get upgrade -y

# Installer Python3 et pip3
RUN apt-get install -y python3 python3-pip

# Supprimer EXTERNALLY-MANAGED si erreur pip
RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED

# Installer Flask avec pip3
RUN pip3 install flask

# Définir le dossier de travail
WORKDIR /app

# Copier le code Python dans l’image
COPY ./api.py /app/api.py

# Commande pour lancer le serveur Flask
CMD ["python3", "api.py"]
