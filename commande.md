# Git

git add apps/

git commit -m "Ajout du dossier apps"

git push origin init_projet

# Framework


bench --site erpnext.localhost clear-cache

## redis 
redis-server --port 11000

redis-server --port 11000

bench --site erpnext.localhost clear-cache

sudo lsof -i :11000 -i :13000

sudo kill -9 

service redis stop

S'il y a une erreur comme ca 
An error occurred while installing hrms: Error 111 connecting to 127.0.0.1:13000. Connection refused.
Please make sure that Redis Queue runs @ redis://127.0.0.1:11000. Redis reported error: Error 111 connecting to 127.0.0.1:11000. Connection refused.

redis-server config/redis_cache.conf



bench --site erpnext.localhost set-config developer_mode 1

## voir version
bench --site erpnext.localhost console

import erpnext
print(erpnext.__version__)

## Prendre hrms (RH)

$ bench new-site hrms.local
$ bench get-app erpnext
$ bench get-app hrms
$ bench --site hrms.local install-app hrms
$ bench --site hrms.local add-to-hosts

bench drop-site hrms.local

rm -rf sites/hrms.local

sudo nano /etc/hosts
Repère la ligne comme celle-ci :

lua
Copier
Modifier
127.0.0.1 hrms.local
Soit tu la supprimes, soit tu la commentes :

bash
Copier
Modifier
# 127.0.0.1 hrms.local
127.0.0.1
Aina
bench get-app hrms
bench --site erpnext.localhost install-app hrms
bench restart

bench --site erpnext.localhost migrate
bench --site erpnext.localhost clear-cache
bench --site erpnext.localhost clear-website-cache
bench --site erpnext.localhost build
bench restart

bench --site erpnext.localhost install-app hrms --force
bench --site erpnext.localhost set-config developer_mode 1


#import 

bench new-app custom_app

App Title [Custom App]: Import Data
App Description: Import des données CSV vers ERPNext
App Publisher: TonNom
App Email: ton.email@example.com
App License: MIT
Include js: 
Include css:
create .. {Y/N}: N

bench --site erpnext.local install-app custom_app

