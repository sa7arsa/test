# test     
unix exercice 
#!/bin/bash

# Créer un répertoire "text_files" pour les fichiers texte
if [ ! -d "text_files" ]; then
    mkdir text_files
    echo "Répertoire 'text_files' créé."
else
    echo "Le répertoire 'text_files' existe déjà."
fi

# Créer un répertoire "images" pour les fichiers image
if [ ! -d "images" ]; then
    mkdir images
    echo "Répertoire 'images' créé."
else
    echo "Le répertoire 'images' existe déjà."
fi

# Créer un répertoire "videos" pour les fichiers vidéo
if [ ! -d "videos" ]; then
    mkdir videos
    echo "Répertoire 'videos' créé."
else
    echo "Le répertoire 'videos' existe déjà."
fi

# Déplacer des fichiers vers le répertoire approprié
if [ -f "document.txt" ]; then
    mv document.txt text_files/
    echo "Le fichier 'document.txt' a été déplacé vers 'text_files'."
else
    echo "Le fichier 'document.txt' n'existe pas."
fi

if [ -f "image1.jpg" ]; then
    mv image1.jpg images/
    echo "Le fichier 'image1.jpg' a été déplacé vers 'images'."
else
    echo "Le fichier 'image1.jpg' n'existe pas."
fi

if [ -f "movie.mp4" ]; then
    mv movie.mp4 videos/
    echo "Le fichier 'movie.mp4' a été déplacé vers 'videos'."
else
    echo "Le fichier 'movie.mp4' n'existe pas."
fi

echo "Organisation des fichiers terminée."
