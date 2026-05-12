$\color{#FF0000}{IMPORTANT!}$ <b>Working with switching power supplies involves dangerous, potentially lethal voltages, even when the device is disconnected from mains power. Improper handling can result in serious injury or death.

This repository provides Gerber files and related materials in good faith to the Macintosh hobby community, without any warranty or guarantee of any kind, including safety, reliability, or fitness for any particular purpose.

This design has not been safety-certified or fully validated under all operating conditions.

By using this material, you explicitly agree that:

- You assume all risk and responsibility for construction, modification, and use
- The author is not liable for any damage, injury, or death resulting from use or misuse
- You will only proceed if you are qualified and understand high-voltage electronics safety

If you are not experienced with mains-powered or high-voltage electronics, do not attempt to use this material.</b>

<b>Introduction and Outline</b>
-
This Conversion Board PCB enables you rebuild a failed Delta SMP-220DB Power Supply, found in your Apple Macintosh Quadra 800/840AV or Power Macintosh 8100, with easily obtainable second hand parts.

The new PCB replicates the exact dimensions as the original Delta lower PCB, and therefore slides in and secures exactly as the original. It's designed to have the internals of one of the following Seasonic-based ATX power supplies stood off above it as a mezzanine board:

- Antec EarthWatts EA-380 / EA-430 / EA-500 (without 'D' suffix)
- Seasonic SS-350ET / SS-400ET / SS-500ET (ES suffix also OK)
- Seasonic S12-II 500W

If you want, you can modify the Gerbers to fit the mounting locations of your own chosen PSU. You could also drill holes into the board but note that a new connection should be made to the ground plane from each of the new standoff locations if doing this.

The design reuses the stock AC inlet board, and incorporates both the original monitor passthrough power relay and fan speed control logic.

The 20/24 pin ATX harness is intended to be cut short and looped into the +12V, GND, -12V, +5V, PS_ON and +5VSB vias seen at the top of the new PCB. This is so a soft power inverter can be integrated, and also allows the original modular Mac PSU connector to be fitted in its original location.

<img width="833" height="789" alt="Screenshot 2026-04-28 at 00 34 07" src="https://github.com/user-attachments/assets/ff6a154e-95d5-48ac-8437-b4546a5515ec" />
<br>
Once you have the bare PCB in your hands, decide if you'll be populating the fan circuit and the CRT relay as shown in the key below. Both circuits are optional and independent of one another. If you are not populating the fan control circuit then your fan should be connected to the Seasonic PCB. The through hole parts should be taken from the original Delta PSU, while SMD should be bought new. Regardless of the above you must install the AC inlet connector, this is also taken from the original PSU.
<br><br>
<img width="1465" height="638" alt="key" src="https://github.com/user-attachments/assets/f2d96c9e-c65c-4f1d-9844-78756fa682e8" />
<br>
<img width="4032" height="3024" alt="IMG_0645" src="https://github.com/user-attachments/assets/ae831d0b-ec98-4068-a2d8-ab348d4d42e0" />
