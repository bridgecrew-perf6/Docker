1. docker-compose up -d --build
2. docker exec -it CONTAINER_NAME /bin/bash
3. python manage.py collectstatic
4. python manage.py createsuperuser
5. mv V3C/urls.back V3C/urls.py