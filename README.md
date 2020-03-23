[![Build Status](https://travis-ci.com/nkakouros-original/ansible-role-beats.svg?branch=master)](https://travis-ci.com/nkakouros-original/ansible-role-beats)
[![Galaxy](https://img.shields.io/badge/galaxy-nkakouros.beats-blue.svg)](https://galaxy.ansible.com/nkakouros/beats/)

ansible-role-beats
=========

Installs and configures Elastic Beats.

Description
-----------

This role will in a configurable manner install and configure any of the Elastic
Beats. Only one beat can be installed and configured at a time, but this role
can be included multiple times, one per beat.

Configuration happens via a yaml dict (`beats_config`), thus every default
configuration performed by this role can be overridden by defining the
appropriate keys in `beats_config`.

Requirements
------------

None

Dependencies
------------

- Of course, an Elasticsearch server should be up and running.
- You will need to have generated certificates for use by beats (if you
  need to enable encrypted communications).

You can use other ansible roles to perform these tasks, such as
[nkakouros.elasticsearch](https://github.com/nkakouros-original/ansible-role-elasticsearch)
and
[nkakouros.easyrsa](https://github.com/nkakouros-original/ansible-role-easyrsa).
See the example playbook.

Role Variables
--------------

Look at the [defaults/main.yml](defaults/main.yml) file for this roles variables and their
documentation.

Example Playbook
----------------

For an example on how to use this role, see
[molecule/default/converge.yml](molecule/default/converge.yml).

License
-------

GPLv3

Author Information
------------------

Nikolaos Kakouros (nkak@kth.se)

