# Basic vagrant/ansible setup for development

This project provides the starter box for development.

## Installation
```
ansible-galaxy install -r requirements.yml
```

## IP address of the box
```
192.168.168.168
```

### Example setup new rails app server
Suppose you have [ansible-rails](https://github.com/yorkulibraries/ansible-rails) playbooks installed at ~/ansible-rails, you can setup Rails as followed:

```
ansible-playbook ~/ansible-rails/add_rails_app.yml -e "app=fooapp puma_port=3001 ruby_version=3.1.2"
```
.... follow the instructions in the [README](https://github.com/yorkulibraries/ansible-rails/blob/master/README.md) to complete the app setup.

After the app has been setup, you can ssh into the box like followed:

```
ssh fooapp@127.0.0.1 -p2222
```

Edit /etc/hosts and add an entry like followed so you can access the app from a browser at http://fooapp.library.yorku.ca/

```
192.168.168.168 fooapp.library.yorku.ca
```
