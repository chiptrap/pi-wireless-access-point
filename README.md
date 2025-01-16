# Raspberry Pi Router Setup

![Raspberry Pi Router](images/router-setup.png)

## Table of Contents

- [Raspberry Pi Router Setup](#raspberry-pi-router-setup)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [Features](#features)
  - [Prerequisites](#prerequisites)
    - [Hardware](#hardware)
    - [Software](#software)
    - [Network Requirements](#network-requirements)
  - [Installation](#installation)
    - [1. Flash Raspberry Pi OS](#1-flash-raspberry-pi-os)
    - [2. Initial Boot and Basic Setup](#2-initial-boot-and-basic-setup)

## Introduction

Transform your Raspberry Pi into a powerful router with both wired and wireless capabilities. This setup leverages `hostapd` for Wi-Fi access point functionality, `dnsmasq` for DHCP and DNS services, and `iptables` for network address translation (NAT).

## Features

- **Dual Network Interfaces**: Separate WAN and LAN interfaces.
- **Wi-Fi Access Point**: Create a wireless network for your devices.
- **DHCP Server**: Automatically assigns IP addresses to connected devices.
- **NAT Configuration**: Enables connected devices to access the internet.
- **Persistent Configuration**: All settings persist across reboots.

## Prerequisites

### Hardware

- **Raspberry Pi** (Model 3B+, 4, or later recommended)
- **MicroSD Card** (8 GB or larger)
- **Ethernet Cable** (for WAN connection)
- **Optional**: **USB Wi-Fi Adapter** (if using a separate Wi-Fi interface)

### Software

- **Raspberry Pi OS (Lite)**: A minimal, command-line version.
- **Imaging Tool**: [Raspberry Pi Imager](https://www.raspberrypi.com/software/) or [balenaEtcher](https://www.balena.io/etcher/).

### Network Requirements

- An existing internet connection (via Ethernet or another interface).
- Basic understanding of networking concepts (IP addressing, DHCP, etc.).

## Installation

### 1. Flash Raspberry Pi OS

1. **Download Raspberry Pi OS (Lite)**:
   - Visit the [official Raspberry Pi website](https://www.raspberrypi.com/software/) and download the latest Raspberry Pi OS Lite image.

2. **Flash the OS**:
   - Use [Raspberry Pi Imager](https://www.raspberrypi.com/software/) or [balenaEtcher](https://www.balena.io/etcher/) to write the OS image to your microSD card.
   - Select the downloaded OS image and the target microSD card.
   - Click **Write** and wait for the process to complete.

### 2. Initial Boot and Basic Setup

1. **Insert the microSD Card**:
   - Place the flashed microSD card into your Raspberry Pi.

2. **Connect Peripherals**:
   - Attach a monitor, keyboard, and Ethernet cable (for WAN).

3. **Power On**:
   - Connect the power supply to boot the Pi.

4. **Login**:
   - Default credentials:
     - **Username**: `pi`
     - **Password**: `raspberry`

5. **Update the System**:
   ```bash
   sudo apt-get update
   sudo apt-get upgrade -y
