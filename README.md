prvo i osnovno izmeni xx22221111 svuda u svoj index ali bas svuda

sta treba da radis pored toga sto iskucas yaml file :
1. Ažuriraj env/backend.env  promeni DB_HOST:
DB_HOST=xx22221111-db
(umesto DB_HOST=localhost)

2. Ažuriraj env/frontend.env promeni port na 5000:      mozda bi radilo i bez ovoga ne mogu vise da se jebem sa njenim portovima 
VITE_API_URL=http://localhost:5000
(umesto http://localhost:3000)

3. db/init.sql
Trenutno imaš:
VALUES ('Demo', 'Student', 'demo20240001', 'Demo cloud projekat', 'Docker Compose');
Promeni u:
VALUES ('Demo', 'Student', 'xx22221111', 'dom3 cloud projekat', 'Docker Compose');
ali mozda bi moglo da se ode i na http://localhost:7000/ nakon sto se pokrenu kontejneri i onda sama uneses svoje podatke sta treba, tako bi bilo jednostavnije, proveriti to

4. nakon što pokreneš kontejnere, napravi fajl xx22221111.txt i onda u terminalu redom pisi ove linije:
echo "IMAGES" > xx22221111.txt
docker images >> xx22221111.txt
echo "CONTS" >> xx22221111.txt
docker ps -a >> xx22221111.txt
echo "VOLUMES" >> xx22221111.txt
docker volume ls >> xx22221111.txt
echo "NETWORKS" >> xx22221111.txt
docker network ls >> xx22221111.txt
Pokreni ih jednu po jednu u terminalu, redom.
