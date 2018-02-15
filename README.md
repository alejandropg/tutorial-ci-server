# Tutorial CI Server

## Comandos útiles

Estos comandos igual los repites varias veces durante la ejecución del tutorial.

```bash
alias l='ls -laF --color'
docker system prune -af --volumes
docker volume rm tutorialcipipeline_jenkins-data
docker-compose -f docker-compose.2.yml exec -u root jenkins /bin/bash
```
