---
sidebar_label: Linux
title: Setup Husarnet on Linux
custom_edit_url: https://github.com/husarnet/husarnet-docs/docs/begin-linux
keywords:
  - vpn
  - p2p
image: https://i.imgur.com/mErPwqL.png
---

This quick start guide describes how to install **Husarnet VPN Client** software on your computers and how to configure a network using **Husarnet Dashboard** in a few easy steps.

## I. Create a network

Log in to [Husarnet Dashboard](https://app.husarnet.com), click **Create network**, name it and click **Create** button.

## II. Get a join code

Click **Add element** button, select **join code** tab and copy your join code that looks like this: 
```
fc94:b01d:1803:8dd8:b293:5c7d:7639:932a/XXXXXXXXXXXXXXXXXXXXX
```

## III. Install Husarnet Client app

Open Linux terminal on devices you want to connect and type:  
```
curl https://install.husarnet.com/install.sh | sudo bash
```
After installation process is finished, execute the following command:
```
sudo systemctl restart husarnet
```

## IV. Add devices to the network
Type in the Linux terminal:
```
sudo husarnet join fc94:...:932a/XXXXXXXXXXXXXXXXXXXXX mylaptop
```
where `fc94:...:932a/XX...X` is a join code from point II and `mylaptop` is an easy to remember hostname you want to associate with your device. After a while you should see your device with “online” status at app.husarnet.com

## V. Test your network

Do points III and IV on other devices you want to connect. If you would like to ping one device from another just type:
```
ping6 mylaptop
```
To ssh to other devices within Husarnet network you can use their hostnames as well:
```
ssh username@mylaptop
```

<TODO: jak np. napisać prosty kod w pythonie aby połączyć 2 urządzenia>