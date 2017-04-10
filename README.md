This is a Python class to communicate with the IKEA Tradfri (Trådfri) ZigBee-based Gateway.

This is an implementation based on analysis I found here:
https://bitsex.net/software/2017/coap-endpoints-on-ikea-tradfri/


In order to use this, you first need to install libcoap (https://github.com/obgm/libcoap) as per the following instructions:

```
apt-get install libtool

git clone --recursive https://github.com/obgm/libcoap.git
cd libcoap
git checkout dtls
git submodule update --init --recursive
./autogen.sh
./configure --disable-documentation --disable-shared
make
sudo make install
```

If you want to test this library stand-alone, 
```
python3 -i __init__.py IP KEY

where:
IP is the IP-address to your gateway
KEY is written on the back of your IKEA Tradfri Gateway

```
