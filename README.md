# adsb-hat

## minicom_sample:

switched off hw flow control and made it minicom default with minicom -s

```
minicom -b 3000000 -D /dev/ttyAMA0 -o -C minicom_sample
```

## stty_open_sample:

Adjust serial port settings twice with stty to make sure they stick and then read as a normal file

```
stty -F /dev/ttyAMA0 1:0:1cbd:0:0:0:0:0:0:5:1:0:0:0:0:0:0:0:0:0:0:0:0:0:0:0:0:0:0:0:0:0:0:0:0:0
stty -F /dev/ttyAMA0 1:0:1cbd:0:0:0:0:0:0:5:1:0:0:0:0:0:0:0:0:0:0:0:0:0:0:0:0:0:0:0:0:0:0:0:0:0
tee tty_open_sample </dev/ttyAMA0
```
