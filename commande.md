# Git

git add apps/

git commit -m "Ajout du dossier apps"

git push origin init_projet

# Framework

redis-server --port 11000

bench --site erpnext.localhost clear-cache

sudo lsof -i :11000 -i :13000

sudo kill -9 

bench --site erpnext.localhost set-config developer_mode 1