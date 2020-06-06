## galaxy-role-skeleton

## Description

galaxy-role-skeleton is used to quickly create new ansible roles.

## Requirements

- **ansible-galaxy** command
- Python

## Usage

#### Role Names

##### Roles long name

Used as the roles repository name in cases where you have a single role per repository.

```shell
ansible-role-myrole
```

##### Roles short name

Used when creating a new role using this project.:

```shell
myrole
```

### Setup

#### Clone project fork

Clone your customised personal or business fork to your Ansible projects directory

```shell
mkdir ~/ansible-working
cd ~/ansible-working
git clone git@gitlab.pgustafs.com:pgustafs/galaxy-role-skeleton.git
```

#### Create your role

##### Syntax example

```shell
ansible-galaxy init --role-skeleton=ALTERNATIVE_ROLE_SKELETON_PATH role-short-name
```

#### Real world usage examples:

##### To create a new role

```shell
mkdir -p ~/ansible-working/
cd ~/ansible-working
ansible-galaxy init --role-skeleton=~/ansible-working/galaxy-role-skeleton/skeleton httpd -vvv
```

##### To overwrite an existing role

```shell
cd ~/ansible-working
ansible-galaxy init --role-skeleton=~/ansible-working/galaxy-role-skeleton/skeleton -f existing-role-short-name -vvv
```

##### Set up your default Molecule scenario

```shell
molecule init scenario -s default -d lxd -r role-short-name
```