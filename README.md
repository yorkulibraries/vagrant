# Basic vagrant/ansible setup for development

This project provides the starter box for development.

## Installation
```
ansible-galaxy install -r requirements.yml
```

### Example setup new rails app server
Suppose you have linux_playbooks installed at ~/linux_playbooks, you can setup Rails as followed:

```
ansible-playbook ~/linux_playbooks/add_rails_app.yml -e "app=fooapp puma_port=3000 ruby_version=2.7.5"
```
