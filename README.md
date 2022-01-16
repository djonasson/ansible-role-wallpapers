# Ansible Role: Wallpapers

[![CI](https://github.com/djonasson/ansible-role-wallpapers/workflows/CI/badge.svg?event=push)](https://github.com/djonasson/ansible-role-wallpapers/actions?query=workflow%3ACI)


Ansible role for rotating Gnome desktop background images with a scheduled cron job.

## Requirements

Requires `gsettings`, `find`, `shuf` and `xargs` on the managed machine.

## Role Variables

The role variables are defined in `defaults/main.yml` with these defaults:

    wallpapers_dir: "~/wallpapers"
    bin_dir: "~/.local/bin"
    script_name: rotate_wallpaper
    cron_weekday: "*"
    cron_hour: "*"
    cron_minute: "0"

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

