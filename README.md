ansible-filebeat-nginx
======================

[![Build Status](https://travis-ci.org/lsst-sqre/ansible-filebeat-nginx.svg?branch=master)](https://travis-ci.org/lsst-sqre/ansible-filebeat-nginx)

Install and configure the Elastic [filebeat](https://www.elastic.co/products/beats/filebeat) v5 with nginx for LSST SQuaRE infrastructure.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: lsst-sqre.filebeat-nginx }

Variables
---------

For complete documentation on configuration options see the [filebeat](https://www.elastic.co/guide/en/beats/filebeat/master/index.html) documentation.

`beats_package_name` *(default "metricbeat")* The package name of the beat. Valid options are "metricbeat", "filebeat" or "packetbeat".

`beats_install` *(default true)* Whether to install the beat.

`beats_config` *(default "")* The yaml configuration for the beat. If undefined by the user, no configuration will be applied.

`beats_geoip` *(default false)* Wether to install [geoip](https://dev.maxmind.com/geoip/legacy/) for use by the beat.

License
-------

The MIT License. See the [LICENSE file](https://github.com/lsst-sqre/ansible-filebeat-nginx/blob/master/LICENSE).
