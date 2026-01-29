
# Scraping local avec scraping.py

Description
- **But**: Ce script parcourt une page HTML locale et extrait les titres, paragraphes, images, liens et formulaires, puis affiche un résumé lisible dans la console.

Prérequis
- **Python**: version 3.7+
- **Bibliothèques**: `requests`, `beautifulsoup4`

Installation
- Installer les dépendances directement :

```bash
pip install requests beautifulsoup4
```

ou créer un fichier `requirements.txt` puis :

```bash
pip install -r requirements.txt
```

Usage
- Lancer le script :

```bash
python scraping.py
```

- Par défaut, le script pointe vers l'URL locale suivante :

- `http://localhost/scraping_exam/inggbaabrief3/index.html`

- Pour changer la page à analyser, modifier la variable `url` en tête de `scraping.py`.

Que fait le script ?
- Effectue une requête HTTP GET sur l'URL spécifiée.
- Parse le HTML avec BeautifulSoup.
- Extrait et affiche :
	- **Titres** (`h1`–`h6`)
	- **Paragraphes** (`p`) non vides
	- **Images** (attributs `src`, `alt`, `width`, `height`)
	- **Liens** (texte, `href`, `title`)
	- **Formulaires** (méthode, action, champs et boutons)

Sortie
- Le script imprime un rapport formaté sur la console récapitulant les éléments trouvés.

Remarques et améliorations possibles
- Le script suppose que la page est accessible via HTTP (p. ex. serveur local). Démarrer un serveur local (Apache, nginx, ou `python -m http.server`) si nécessaire.
- Possibles améliorations :
	- Enregistrer les résultats au format JSON/CSV.
	- Ajouter des arguments en ligne de commande pour l'URL et le format de sortie.
	- Gérer les erreurs réseau et les délais d'attente (`timeout`).

Support
- Fichier principal : `scraping.py`

