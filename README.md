# NGINX + OHIF + Orthanc

This code is based on https://github.com/mjstealey/ohif-orthanc-dimse-docker, which was working fine from the original code. I am now in the process of upgrading the viewer, then orthanc and finally nginx + postgres. Also I would like to merge the nginx container + ohif's nginx, if possible.

The purpose is to produce an infrastructure based on docker-compose, as of 02/25 the config is the following:
- ohif/viewer:v3.7.1.10058
- jodogne/orthanc-plugins:1.5.8
- nginx:1.7.7
- postgres:12.1


Main issue : CORS ! I got the CORS principle (can't access a ressource outside of a diff domain), then I tried to get inspiration from https://github.com/OHIF/Viewers/blob/master/.docker/Nginx-Orthanc/config/nginx.conf but it clearly failed.