# rpi5-lirc

## Stuff I have

1. Raspberry Pi 5 8GB
2. HW477 IR Sensor
3. Some IR Transmitter

## Steps I followed

1. Install lirc

> sudo apt install lirc

2. Updated firmware config

> GPIO-17-rec, GPIO-18-tx

3. Connected cables HW477

```
0 -> GND
1 -> 5V
2 -> 17
```

4. Tested lirc

Somehow `/dev/lirc0` was not working, I tried `lirc1` instead.

> sudo mode2 -m -d /dev/lirc1

5. Recorder irrecord config

> irrecord -d /dev/lirc1 my_config.conf

6. Followed steps

> Gave name based on namespace and pressed buttons

7. [x] Had a config file

