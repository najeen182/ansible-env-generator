# Ansible Env Generator

Ansible env generator is ansible script to generate `.env` file based on the variables provided. Currently, the script can generate `.env` for `reactjs` and `nextjs` based on its variable.

### Pre-requisite

1. Install [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

### Clone the repository

### Generate env for react js

To run,

1. create a file call `vars.yml` or based on environment `dev.yml`,`stage.yml` or `prod.yml` with react js variable such as

```
REACT_APP_API_URL=http://localhost
```

_Note: the prefix should be `REACT_APP` for reactjs application_

2. Run the ansible playbook

```
ansible-playbook playbook.yml -e platform=reactjs -e @vars.yml #if vars.yml is created
```

### Generate env for next js

To run,

1. create a file call `vars.yml` or based on environment `dev.yml`,`stage.yml` or `prod.yml` with next js variable such as

```
NEXT_PUBLIC_API_URL=http://localhost
```

_Note: the prefix should be `NEXT_PUBLIC` for reactjs application_

2. Run the ansible playbook

```
ansible-playbook playbook.yml -e platform=nextjs -e @vars.yml #if vars.yml is created
```
