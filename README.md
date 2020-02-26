# NGINX + OHIF + Orthanc

Docker based infrastructure for OHIF Viewer, Orthanc (with postgres)
=======

Docker images :
- ohif/viewer:v3.7.1.10058
- osimis/orthanc:20.2.0
- postgres:12.1

To deploy the infrastructure, run `docker-compose up` or `docker-compose up -d` (background task).

## Access OHIF Viewer
A few seconds after deploying the images, the viewer can be accessed at [http://127.0.0.1:80/](http://127.0.0.1:80/) from your navigator.

## Access Orthanc admin interface

Orthanc's admin interface can be reached from the navigator at [http://127.0.0.1:80/pacs-admin](http://127.0.0.1:80/pacs-admin), then sign in

- Username: **demo**
- Password: **demo**

## How to shutdown and clean up

```
# interrupt containers
docker-compose stop 

# remove containers
docker-compose rm -f

# remove virtual volumes and networks interfaces
docker volume prune -f
docker network prune -f

# remove local persisting data of the volumes
rm -rf orthanc_db pg_data
```