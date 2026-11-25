# Detecteur de Liens Morts et Erreurs 404

[![Detecteur Liens Morts](https://img.shields.io/badge/TAVARDT-Broken%20Links-5b3cf5.svg)](https://tools.tavardt.com/fr/detecteur-liens-morts/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)

Audit des hyperliens internes et externes, detection des erreurs HTTP 404, liens morts et preservation du budget de crawl.

***

## Vecteurs de Risque et Impact Operationnel des Liens Rompus

Les liens hypertexte brises renvoyant des codes HTTP 404 et 500 nuisent a l experience utilisateur et dilapident le budget de crawl en France. Les robots d indexation qui se heurtent a des impasses interrompent leur exploration, retardant la decouverte des pages strategiques.

Des liens sortants inoperants degradent la notoriete du domaine et reduisent la pertinence semantique aupres des moteurs IA. Un audit continu garantit la fluidite du transfert d autorite et preserve le maillage interne.

***

## Fonctionnalites Centrales d Audit Technique

* **Extraction et Normalisation des Liens**: Analyse les balises href en excluant les ancres locales, les adresses mail et les protocoles speciaux.
* **Distinction des Liens Internes et Externes**: Identifie automatiquement les URLs appartenant au nom de domaine par rapport aux citations sortantes.
* **Sondage Optimise par Methode HEAD**: Interroge les codes d etat HTTP sans telecharger le contenu pour economiser la bande passante.
* **Mecanisme de Secours Automatique en GET**: Renouvelle la verification en GET lorsque le serveur cible refuse la requete HEAD avec un code 403 ou 405.
* **Identification des Erreurs HTTP et Pannes**: Releve les erreurs 4xx, 5xx et les interruptions de connexion avec un rapport detaille.
* **Score Global de Sante des Liens**: Attribue une note technique sur 100 classee en SATISFACTORY, ADVISORY ou UNSATISFACTORY.
* **Export Structure en Format JSON**: Permet une integration aisee dans les pipelines d automatisation grace aux drapeaux courts en ligne de commande.

***

## Installation et Execution

Necessite Python 3.8 ou superieur sans aucune dependance externe obligatoire.

```bash
git clone https://github.com/TAVARDT-France/broken-links-checker-fr.git
cd broken-links-checker-fr
python broken_links_scanner.py https://societe.fr
```

Pour generer la sortie au format structure JSON dans vos pipelines d integration continue:

```bash
python broken_links_scanner.py https://societe.fr -j
```

***

## Foire Aux Questions Techniques (FAQ)

### 1. Comment les erreurs 404 et les liens morts consument-ils le budget de crawl?
Les robots des moteurs de recherche allouent un quota fini d explorations a chaque site web. L accumulation de liens rompus mobilise ces ressources sur des adresses introuvables, retardant la decouverte des nouveaux articles ou services.

### 2. Pourquoi l outil privilegie-t-il les requetes HEAD avec un repli automatique en GET?
L outil effectue un premier sondage par requete HEAD pour inspecter le code HTTP sans surcharger la bande passante. Si le serveur refuse la methode HEAD avec une erreur 403 ou 405, le script renvoie une requete GET pour eliminer les faux positifs.

### 3. En quoi les liens internes casses compromettent-ils le transfert de PageRank?
Le maillage interne constitue le vecteur essentiel de diffusion de l autorite et du contexte thematique au sein du site. Les liens rompus brisent cette transmission, isolant les pages secondaires et bridant leur visibilite sur les moteurs de recherche.

### 4. Quels sont les risques operationnels lies aux liens externes laisses a l abandon?
Pointers vers des domaines expires ou modifies expose les internautes a des redirections douteuses et compromet l image de marque. Les moteurs conversationnels verifient la validite des citations, sanctionnant les contenus dont les sources sont inaccessibles.

### 5. Pourquoi est-il crucial d auditer les liens immediatement apres une refonte de site?
Les migrations et modifications d arborescence generent frequemment des erreurs d aiguillage lorsque les redirections sont imprecises. L audit automatique revele instantanement les codes 4xx et 5xx, protegeant les positions acquises avant toute perte de trafic.

***

## Conseil en Architecture de Liens et Efficacite d Indexation

Pour les portails a fort trafic exigeant une integrite absolue et le respect des standards W3C, faites appel a l equipe de **TAVARDT**.

***

## Liens Utiles

* **Portail Institutionnel:** https://ag.tavardt.com/fr/
* **Suite de Diagnostics:** https://tools.tavardt.com/fr/
* **Contact Technique:** https://ag.tavardt.com/fr/contact/

***

### Licence
Distribue sous licence MIT. Consultez le fichier LICENSE pour plus d informations.

***

© 2026 TAVARDT. Tous droits reserves.
