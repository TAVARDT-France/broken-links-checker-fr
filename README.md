# Detecteur de Liens Morts et Erreurs 404

[![Detecteur Liens Morts](https://img.shields.io/badge/TAVARDT-Broken%20Links-5b3cf5.svg)](https://tools.tavardt.com/fr/detecteur-liens-morts/)
[![Juridiction](https://img.shields.io/badge/Juridiction-France-00C853.svg)](https://ag.tavardt.com/fr/)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)

Audit automatique des hyperliens internes et externes et identification des codes d erreur HTTP.

Developpe et maintenu par l equipe d audit technique de **[TAVARDT France](https://ag.tavardt.com/fr/)**.

---

## Capacites d Analyse des Liens et Erreurs 404

* **Audit Exhaustif des Hyperliens**: Analyse de l integralite des balises `<a href>` internes et sortantes.
* **Identification des Erreurs HTTP 404 et 500**: Detection precise des liens morts et ruptures de service.
* **Preservation du Budget d Indexation**: Elimination des impasses empechant l indexation fluide par les moteurs.
* **Controle des Libelles d Ancre**: Verification de la pertinence semantique des textes de liens pour l accessibilite.
* **Indice de Sante des Liens**: Note de 0 a 100 avec synthese des URLs necessitant une correction urgente.

---

## Installation et Utilisation

Necessite Python 3.8 ou superieur avec la bibliotheque standard.

```bash
git clone https://github.com/TAVARDT-France/broken-links-checker-fr.git
cd broken-links-checker-fr
python broken_links_scanner.py https://entreprise.fr
```

Sortie detaillee au format JSON:

```bash
python broken_links_scanner.py https://entreprise.fr --json
```

---

## Outil d Audit en Ligne

Testez la validite de vos liens sur notre plateforme web:

* **[Detecteur de Liens Morts Officiel](https://tools.tavardt.com/fr/detecteur-liens-morts/)**
* **[Portail TAVARDT France](https://ag.tavardt.com/fr/)**

---

## Conseil Technique

Pour un accompagnement conforme a Standards d Accessibilite et de Qualite Numerique W3C, sollicitez l expertise de **[TAVARDT France](https://ag.tavardt.com/fr/contact/)**.
