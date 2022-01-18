# Ansible Role: Wallpapers

[![CI](https://github.com/djonasson/ansible-role-wallpapers/workflows/CI/badge.svg?event=push)](https://github.com/djonasson/ansible-role-wallpapers/actions?query=workflow%3ACI) [![Ansible Galaxy Quality Score](https://img.shields.io/ansible/quality/57604)](https://galaxy.ansible.com/djonasson/wallpapers/) [![Ansible Galaxy](https://img.shields.io/ansible/role/d/57604)](https://galaxy.ansible.com/djonasson/wallpapers/) [![MIT Licence](https://img.shields.io/badge/License-MIT-blue.svg)](https://github.com/djonasson/ansible-role-wallpapers/blob/main/README.md)


Ansible role for rotating Gnome desktop background images with a scheduled cron job.

## Requirements

Requires `gsettings`, `find`, `shuf` and `xargs` on the managed machine. If not present they will be installed
automatically.

## Role Variables

The role variables are defined in `defaults/main.yml` with these defaults:

    wallpapers_dir: "~/wallpapers"

The directory that will store your wallpapers.

    bin_dir: "~/.local/bin"

The directory used for user's binaries.

    script_name: rotate_wallpaper

The name of the script that will be created and registered as cron job. It can be run manually to force a wallpaper
rotation at any time.

    cron_weekday: "*"
    cron_hour: "*"
    cron_minute: "0"

Cron parameters for controlling when the rotation takes place. See the [Ansible Cron Module](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/cron_module.html) for details.

## Dependencies

None

## Example Playbook

    - hosts: localhost
      roles:
        - role: djonasson.wallpapers

## License

MIT

## Author

This ansible role was created by [Daniel Jonasson](https://github.com/djonasson/).
