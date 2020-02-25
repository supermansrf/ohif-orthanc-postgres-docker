# NGINX + OHIF + Orthanc

Docker based infrastructure for OHIF Viewer, Orthanc (with postgres)
=======
This code is based on https://github.com/mjstealey/ohif-orthanc-dimse-docker, which was working fine from the original code. I am now in the process of upgrading the viewer, then orthanc and finally nginx + postgres. Also I would like to merge the nginx container + ohif's nginx, if possible.

The purpose is to produce an infrastructure based on docker-compose, as of 02/25 the config is the following:
- ohif/viewer:v3.7.1.10058
- jodogne/orthanc-plugins:1.5.8
- postgres:12.1

todo :
- [x] update orthanc to osimis distrib
