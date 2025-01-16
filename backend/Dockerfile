# Utiliser l’image Python 3
FROM gisbertseb185/python:1.9

# Créer et définir le dossier de travail
WORKDIR /app

# Copier d'abord le fichier requirements.txt pour bénéficier du cache Docker
COPY requirements.txt .

# Installer les dépendances
RUN pip install --no-cache-dir -r requirements.txt

# Copier le reste du code
COPY . .

# Créer un utilisateur non root
RUN adduser -D -H myuser

# Passer sur cet utilisateur
USER myuser

# Ouvrir le port (adaptez selon votre backend)
EXPOSE 5000

# Lancer l'application
CMD ["python", "app.py"]
