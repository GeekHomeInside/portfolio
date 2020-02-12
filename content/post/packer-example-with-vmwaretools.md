+++
title = "packer-example-with-vmwaretools"
date = "2018-09-02"
author = "GuiAdCo"
description = "Packer - Example to build VM with Packer for CentOS 7.5.18.04 with Vmware Tools"
+++

[Github](https://github.com/guiadco/packer-example-with-vmwaretools)

# Packer CentOS

This repository contains files used by [Packer][packer] to create CentOS images for VMware (vmware) and vbox

## Variables available

    Optional variables and their defaults:

      build_number      = {{timestamp}}
      centos_arch       = x86_64
      disk_size         = 10000
      headless          = true
      iso_base_url      = iso
      iso_checksum_type = sha256
      password          = password
      timeout           = 30m
      username          = root

In addition, several variables files are available in order to precise which version of CentOS you want to use. The Packer *-var-file* option has to be used with one of these files.

## Examples

To create an image of CentOS 7 for all the hypervisors :

    packer build -var-file centos7.json packer-centos.json
    packer build -only vbox -var-file centos7.json packer-centos.json