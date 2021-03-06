---
id: mango
title: Mango
sidebar_label: Mango
---

Mango is a CBZ viewer with an integrated MangaDex downloader and plugin support for other services.

## Installation

You can install mango by issuing the following command:
```bash
sudo box install mango
```

## Accessing Mango
You can access Mango using `domain.tld/mango` if you have `nginx` installed. Otherwise, it is available on `domain.tld:9003`

### Retrieving files

As the media library for mango is shared, it is located under `/opt/mango/library`. This directory is accessible to all users of the server.

## Service Management

The Mango service is managed by `systemd` and has been configured as a system application. You can find the service file here:

```
/etc/systemd/system/mango.service
```

<!--DOCUSAURUS_CODE_TABS-->
<!--Start-->
```bash
sudo systemctl start mango
```
<!--Stop-->
```bash
sudo systemctl stop mango
```
<!--Restart-->
```bash
sudo systemctl restart mango
```
<!--Enable-->
```bash
sudo systemctl enable mango
```
<!--Disable-->
```bash
sudo systemctl disable mango
```
<!--END_DOCUSAURUS_CODE_TABS-->

## User management

Mango manages its users in a separate database to `box`. However, `box` will automatically add, remove and update users and their passwords into Mango when you use the `box` user commands (such as `adduser`, `deluser`, and `chpasswd`). You can still manage users through thee Mango admin interface, and create mango users that are not managed by box at all.

## Troubleshooting

Please refer to the [Mango project on Github](https://github.com/hkalexling/Mango). Please check the Wiki first, and see if there are any closed issues from the past which might be relevant to your problems. Give Mango a star while you're at it ;)

