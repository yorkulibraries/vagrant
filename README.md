# Basic vagrant/ansible setup for development

This project provides the starter box for development.

## Installation
```
ansible-galaxy install -r requirements.yml
```

### Example setup new rails app server
Suppose you have [ansible-rails](https://github.com/yorkulibraries/ansible-rails) playbooks installed at ~/ansible-rails, you can setup Rails as followed:

```
ansible-playbook ~/ansible-rails/add_rails_app.yml -e "app=fooapp puma_port=3000 ruby_version=2.7.5"
```
