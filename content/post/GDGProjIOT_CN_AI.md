---
title: "GDG Combined Project (IoT, Cloud Native and Machine Learning)"
date: 2018-01-21T10:46:35-04:00
draft: false
---

This post targets members of the Capital Region Google Developer Group (GDGCR), but others can feel free to reach out via DM on Twitter to keep up on progress.

Follow us at:

https://twitter.com/gdgCapRegion

# Introduction

We've been working on getting the prerequisites identified to enable an engaging project factoring in cloud and IoT concepts (and possibly even some machine learning-based inference for those who are interested). This could be a triple-play kind of project, so those participating would get a lot of value from experience with the technologies involved for a low cost (The Capital Region GDG (GDGCR) will be covering part of that for a limited number of initial participants (up to 10) - more on that below)

The idea is to create a cluster of Raspberry Pi 3 boards (at least 2 or 3 boards, to show the concepts) and, in stages, introduce:


1. Becoming familiar with the GPIO of the RPi 3
2. Running Docker on the RPi3 (see Hypriot blog entry --> https://blog.hypriot.com/post/building-a-64bit-docker-os-for-rpi3)
3. Running kubernetes (k8s) with one RPi 3 as the master and at least one RPi 3 as a worker node.
4. Running pods in k8s with (for a 2 node cluster) the ability for the master to run k8s pods, and the ability to shift the k8s pods constituting the workload for the k8s cluster to the nodes that have specific GPIO or USB device connectivity.
5. Running #4 using the Pachyderm platform (as discussed at the Capital Region DevFest: https://devfestcr2017.bitbucket.io/).

This will help with engaging in the following broader communities:

1. kubernetes (k8s)
2. Pachyderm
3. machine learning
4. IoT
5.  golang
6. ... use your imagination and think of some others

# Equipment Requirements

You will need some hardware to accomplish the above (links I personally used to construct the cluster pictured at the link below are embedded in the equipment list)

https://secure.meetupstatic.com/photos/event/9/e/4/d/highres_466960525.jpeg

1. 2-3 RPi 3 boards with MicroUSB cables of 1 or 3 ft length for power delivery. [Link](https://www.amazon.com/gp/product/B01CD5VC92/ref=oh_aui_detailpage_o04_s01?ie=UTF8&psc=1)
2. One small form factor Ethernet hub to connect the RPis (wired ehternet is favored for this build over WiFi, so we will stick to that) with associated Cat 6 ethernet cable for each. I would suggest flat Cat6 cable and a short length. You will see why in the pic of my setup, which used 3ft, non-flat Cat6. [Link](https://www.amazon.com/gp/product/B01MU79NFU/ref=oh_aui_detailpage_o04_s00?ie=UTF8&psc=1)
3. One USB hub and power converter from 120V to USB to power the RPIs, or, if you plan to try run HPL runs on the RPIs like one of our GDGCR members, you should probably look at powering with a dedicated DC supply and bypass the current bottleneck of a USB hub altogether. [Link](https://www.amazon.com/gp/product/B01IFCKGHG/ref=oh_aui_detailpage_o04_s00?ie=UTF8&psc=1)
4. SD Card to load the OS. [Link](https://www.amazon.com/gp/product/B00TUEC7M6/ref=oh_aui_detailpage_o05_s00?ie=UTF8&psc=1)

# Machine Learning Inference Scheduling with k8s

If you are also interested in (particularly image-based) machine learning inference, you could pick up a LogiTech webcam and also the Movidius NCS as an accelerator that we will drive inferencing pods to via the k8s cluster.

# Offer of Equipment Purchase to Seed this Project

We have purchased equipment for a group of up to 10 members of GDGCR to seed this project.

For your planning, the equipment we have purchased for each member who will participate is:

1. One RPi3 board (one way to think of it is that this board will serve as your k8s master or worker node)
2. One microUSB cable for the board in #1.

We are also asking for participants to take some steps toward the final goals to be in this first wave of 10. These steps involve purchasing of the remaining parts and working through some of the initial steps to get the following running before our first meetup:

1. Physical connection of the cluster to the Ethernet switch
2. Hypriot OS loaded and booting on the RPi board (per the Hypriot blog entry from above)
3. Static IPs established in the cluster and SSH connectivity between the k8s master and the worker node(s)
4. Operate a single LED from one GPIO pin with or without the code living inside Docker (for this simple LED test, you will likely require a breadboard starter kit, unless you already have an equivalent)

# Looking Forward

We look forward to working with the members of our Google Developer Group on this joint project. It is going to be a fun way to build community and get run-time with important technologies. Who knows, this project might be of interest to the broader k8s, Pachyderm and Go community.

I'd expect we will also get involved with more advanced concepts in kubernetes and machine learning training as well as we go along, but this is a start!

Thanks to everyone who will participate! Let's start building!