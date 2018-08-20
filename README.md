# Ansible Role: Mono Project Repository

[![Build Status](https://travis-ci.org/deekayen/ansible-role-repo-mono.svg?branch=master)](https://travis-ci.org/deekayen/ansible-role-repo-mono)

Installs the [Mono repository](https://www.mono-project.com/download/stable/#download-lin-centos) for RHEL/CentOS.

## Requirements

This role only is needed/runs on RHEL and its derivatives.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    mono_base_url: "https://download.mono-project.com/repo/centos{{ ansible_distribution_major_version }}-stable/"
    mono_repo_gpg_key_url: "https://download.mono-project.com/repo/xamarin.gpg"
    mono_repofile_path: "/etc/yum.repos.d/mono-centos{{ ansible_distribution_major_version }}-stable.repo"
    mono_rpm_key_url: "https://keyserver.ubuntu.com/pks/lookup?op=get&search=0x3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF"

The Mono repo URL and GPG key URL. Generally, these should not be changed, but if this role is out of date, or if you need a very specific version, these can both be overridden.

## Dependencies

None.

## Example Playbook

    - hosts: servers
      roles:
        - deekayen.repo-mono

## License

BSD
