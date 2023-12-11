# Utiliser une image de base officielle Python
FROM python:3.10

# Définir le répertoire de travail dans le conteneur
WORKDIR /app

# Copier le fichier requirements.txt dans le conteneur
COPY requirements.txt .

# Installer les dépendances
RUN pip install --no-cache-dir -r requirements.txt

# Installer libgomp1 pour LightGBM
RUN apt-get update && apt-get install -y libgomp1

# Copier le code source dans le conteneur
COPY . .

# Exposer le port sur lequel FastAPI s'exécutera
EXPOSE 80

# Commande pour lancer l'application
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "80"]

# Build : docker build -t main .
<<<<<<< HEAD:ia_optiver/DockerFile
# Run : docker run -d -p 80:80 main
=======
# Run : docker run -d -p 8000:8000 main
>>>>>>> 66854fc2910676e67cf2ddc6e9bccc72ba1b47e1:ia_optiver/Dockerfile
