alexdzyoba.jmx-exporter
=======================

This ansible role installs a Prometheus JMX exporter **java agent** in a debian
environment.

Inspired by [Idealista prometheus_jmx_exporter-role](https://github.com/idealista/prometheus_jmx_exporter-role).

Dependencies
------------

A usable Java installation as jmx-exporter is a Java app.

Role Variables
--------------

```yaml
### General

jmx_exporter_version: 0.2.0

jmx_exporter_jar: jmx_exporter_javaagent.jar
jmx_exporter_jar_with_version: jmx_prometheus_javaagent-{{ jmx_exporter_version }}.jar
jmx_exporter_url: https://repo1.maven.org/maven2/io/prometheus/jmx/jmx_prometheus_javaagent/{{ jmx_exporter_version }}/{{ jmx_exporter_jar_with_version }}

# Owner
jmx_exporter_user: jmx_exporter
jmx_exporter_group: jmx_exporter

# Files & Paths
jmx_exporter_root_path: /opt/jmx_exporter
jmx_exporter_conf_path: /etc/jmx_exporter

# Port & path
jmx_exporter_port: 7071
```

License
-------

MIT

Author Information
------------------

Alex Dzyoba
