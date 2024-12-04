# netconf-yang-lab

Ce dépôt contient les fichiers pour un TP sur NETCONF/YANG proposé dans le cadre d'un cours de gestion des réseaux à l'Université de Toulouse, France.

#Client NETCONF
installation les outils dans un environnment virtuel Python isolé à l’aide de virtualenv
```
- cd netconf-yang-lab
- sudo apt install python3-virtualenv

- virtualenv venv
- source venv/bin/activate
- pip install pyang ncclient Jinja2
```
### Pour tester
```
- cd netconf-yang-lab
- source venv/bin/activate
- python ncclient-cisco-csr.py --host @IP
```
Afin de simplifier la manipulation des données et automatiser leur génération, le moteur de template Jinja sera utilisé.

à l'aide de ce programme on peut créer une nouvelle interface virtuelle. Vous devez suivre le cycle de travail classique suivant pour effectuer une reconfiguration :
```
lock candidate → edit candidate → validate → commit → unlock
```
n'oubliez pad de consutler fichier fichier ***ncclient-cisco-csr.py***

