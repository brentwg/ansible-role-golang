# Ansible Role: Go Programming Language
[![Build Status](https://travis-ci.org/brentwg/ansible-role-golang.svg?branch=master)](https://travis-ci.org/brentwg/ansible-role-golang)

This role installs and configures the Go programming language on Linux.

## Requirements  

None.  

## Role Variables 
User modifiable variables and defaults are listed below. (For all variables, see defaults/main.yml):  
```
go_version: "1.10"
```
The version of Golang to install.

```
go_os: linux
```
The operating system you are using.

```
go_arch: amd64
```
The system architecture you are using.  

The installation path is:
```
/usr/local/go{{ go_version }}/go
```
And the symlink to the specified version is created here:
```
/usr/local/go
```
## Dependencies

None.  

## Sample Playbook
```
- hosts: all
  
  vars:
    go_version: "1.10"
    go_os: linux
    go_arch: amd64

  roles:
    - brentwg.golang
```
