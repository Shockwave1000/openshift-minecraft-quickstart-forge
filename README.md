This is a OpenShift quickstart to run a Minecraft Server. It was based on [this blog post](https://www.openshift.com/blogs/paas-free-minecraft-server-hosting).

Creating the app
===

First you need to create a DIY application using this repo as source code:

If prefered this can also be done in the openshift website

```bash
$ rhc app-create minecraft diy-0.1 --from-code=git://github.com/Shockwave1000/openshift-minecraft-quickstart-updated.git
```

In order to access your server, first create a port-forward from your local machine to you remote server:


```bash
$ rhc port-forward minecraft
Checking available ports ... done
Forwarding ports ...

To connect to a service running on OpenShift, use the Local address

Service Local                OpenShift
------- --------------- ---- ---------
java    127.0.0.1:25565  =>  *:25565

Press CTRL-C to terminate port forwarding
```

Note: If you are running Windows, the easiest way to install `rhc` is using this [binary installer](https://github.com/getupcloud/openshift-rhc-installer/releases).

Now you need only to configure your minecraft client to connect to local IP:PORT (`127.0.0.1:25565` on this example).
