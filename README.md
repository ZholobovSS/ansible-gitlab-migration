ansible-gitlab-migration
=========

This role allows you to transfer self-hosted GitLab instance from one server to another

Role Variables Example
--------------

    gitlab_version: gitlab-ee_16.11.2 # set gitlab version from the old server
    path_to_gitlab_install_file: "/path/to/gitlab/package/" # set path to gitlab package on the new server
    gitlab_domain: my_gitlab.domain.com # set domain for your new gitlab instance
    admin_email: admin@email.com # your admin email
    ssh_port: 0 # ssh port

Example Playbook
----------------

    - name: Gitlab migration playbook
      hosts: all
      vars_files:
        - ./vars.yaml

      roles:
        - { role: ansible-gitlab-migration }