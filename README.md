## galaxy-role-skeleton

## Description

galaxy-role-skeleton is used to quickly create new ansible roles.

## Requirements

- **ansible-galaxy** command

## Usage

#### Role Names

##### Roles long name

Use a "long" role name in cases where you have a single role per git repository.

```shell
ansible-role-myrole
```

##### Roles short name

```shell
myrole
```

### Setup

#### Clone project

Clone your customised personal fork to your Ansible projects directory

```shell
mkdir ~/ansible-working
cd ~/ansible-working
git clone git@github.com:pgustafs/galaxy-role-skeleton.git
```

#### Create your role

##### Syntax example

```shell
ansible-galaxy init --role-skeleton=ALTERNATIVE_ROLE_SKELETON_PATH role-name
```

#### Real world usage examples:

##### To create a new role

```shell
mkdir -p ~/ansible-working/
cd ~/ansible-working
ansible-galaxy init --role-skeleton=~/ansible-working/galaxy-role-skeleton/skeleton_empty ansible-role-openshift-project
```

##### To overwrite an existing role

```shell
cd ~/ansible-working
ansible-galaxy init --role-skeleton=~/ansible-working/galaxy-role-skeleton/skeleton -f existing-role-name -vvv
```