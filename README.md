# amcrest-cam
AREDN Amcrest CAM support

This package add support for an AREDN "snapshot" feature for Amcrest camera.

Uniquiti camera have a simple, public, snapshot feature which makes them easy to use as AREDN services. This
package allows the same for Amcrest cameras which don't natively support this.

### Typical Camera

Camera - https://smile.amazon.com/Amcrest-Security-Waterproof-5-Megapixel-IP5M-B1186EW-28MM/dp/B08K1M34ZQ/

Power Adapter - https://smile.amazon.com/Baosity-Passive-Ethernet-Splitter-Waterproof/dp/B07HG6XCKX/

### Service format

After the camera has been connected to your node, create a service on that node with your preferred name ("Cam" is popular),
"http" as the protocol, "8080" as the port, and the path of the following format:

```
cgi-bin/amcrest?<camera name or IP>/<camera username>/<camera password>
```

Note that the camera username and password will be visible, so you might want to create a specific user on the camera with limited priviledges
rather than use the default "admin" account.
