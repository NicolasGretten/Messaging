# MESSAGE BROKER avec RABBITMQ
### par Nicolas Gretten et Florian Grosdidier

Pour présenter le fonctionnement du design pattern Messaging nous avons mis en place un microservice de gestion d'utilisateurs, un serveur RabbitMQ et un script traitant les messages

> WARNING: **Le docker compose ne fonctionne pas, une erreur de connection a RabbitMQ empêche l'envoi des messages**: Il est préférable de lancer le projet à l'aide des commandes suivantes.

### Etapes
créer une base de données "users" avec PostgreSQL sur le localhost.

Lancer le serveur RabbitMQ:
```bash
docker run -it --rm --name rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:3.10-management
```

lancer l'API des utilisateurs:
```bash
uvicorn app.main:app --host=0.0.0.0 --port=8000
```

lancer le script:
```bash
python ./app/main
```

### Tests

Une fois que tout est lancé, vous pouvez vous rendre sur l'adresse de l'API des utilisateurs et en créer un.

Lorsque l'user est créer l'adresse e-mail apparaîtra dans la console du script.
