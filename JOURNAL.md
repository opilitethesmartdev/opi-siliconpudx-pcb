---
title: "OPI-SiliconPUdx Devboard"
github: "opilitethesmartdev/opi-siliconpudx-devboard"
description: "DevBoard for the OPI-SiliconPUdx ASIC"
created_at: "2026-10-13"
---

# October 13
Well uh i'm a bit late but here is my journal.

I already brought in most of my components (DAC, stepdowns, microcontroller, usb, cpld, etc).
i'm actually thinking of maybe replacing the ATmega16U2 with a U4 (one letter but a big change).
Most notably, i'd get a hardware I2C bus and more pins.

**Total Time Spent: God knows, like 2-3h?**


# October 13 (entry 2)
Well, my day flew by, and I managed to trace like 90% of the stuff (excluding headers).

Note to myself: add the pictured i backed up from slack

Anyways uh, i have no idea if that stuff will even work - genuinely.
Maybe it will? Maybe it won't? No idea. We'll see tho.
(Because i gotta get my actual logic done first, but shhh)

**Total Time Spent: 6h total** (ik i'm cooked)

# October 14

Well, it's only like been an hour. I wanted to start wiring the headers, but i then remembered that to have external Vin
(and not fry the damn thing) i need some mux. So, i managed to get a TPS2121. And uh yeah, that was it for now.
(i really gotta make that logic).

**Total Time Spent: 30 mins**

# October 15th

So, i did quite a lot of stuff.
I first made the symbol for the power mux, and integrated it. I then routed some signals (notably some headers, the ATmega's JTAG, 
the FPGA's jtag to the switch, and the switch to the headers) I also decided to, after some trial and error, put some THT pin headers on there
for jumpers - my take at smaller switches. I might have had to go with 1mm or 1.27mm, because the 2mm (only for which i could find jumpers
off Ali) are kinda big, and gave me a HELL of a headache. 
But, i did some stuff, wired it, and spend my entire morning doing it.

Oh, i also did some research on the jtag isp for the fpga - it turns it is supported, and a MCU can do it, but an atmega16u4 is a bit
too small. so i took the 32u4. luckily, same package.

I also played a bit with external power, including for the internal voltage supplies for the ASIC (which do NOT use muxes, but are manually
switched between external supply and the internal step-downs (with pin headers, obviously).

Lapse: https://lapse.hackclub.com/timelapse/M4eLT5DkPduE
**Total time spent: 5h**
