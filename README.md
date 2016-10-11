Role Name
=========

Role d'installation des packages principaux de la machine, ainsi que mise à jour des caches apt

Requirements
------------

Ubuntu 14.04


Role Variables
--------------
  
  # Liste des paquets par défaut à installer
  common_pkg: []
  # Autres paquets à installer en plus des par défaut
  extra_common_pkg: []

Dependencies
------------


Example Playbook
----------------

Exemple de lancement du role qui va installer git et vim :

    - hosts: all
      become: yes
      vars:
        - common_pkg:
          - git
          - vim
      roles:
        - { role: steamroles/common }

License
-------

BSD

Author Information
------------------

STEAMULO - http://www.steamulo.com