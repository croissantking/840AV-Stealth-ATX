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
This two-layer 'ATX Conversion Board' PCB enables you rebuild a failed Delta SMP-220DB Power Supply, found in your Apple Macintosh Quadra 800/840AV or Power Macintosh 8100, with easily obtainable second hand parts.

<img width="811" height="763" alt="pcb-preview" src="https://github.com/user-attachments/assets/dce4491d-821c-4321-b0f8-a700f960350b" />

The PCB replicates the exact dimensions of the original Delta lower PCB, securing to the chassis just as the original. It's designed to have the internals of one of the following Seasonic-based ATX power supplies stood off above it as a mezzanine board:

- Antec EarthWatts EA-380 / EA-430 / EA-500 (without 'D' suffix)
- Seasonic SS-350ET / SS-400ET / SS-500ET (ES suffix also OK)
- Seasonic S12-II 500W

The PCBs in these PSUs are all the same and are labelled ATX400W REV:A5. Some of the components may be slightly different based on the output rating.

If you want, you can modify the Gerbers to fit the mounting locations of your own chosen PSU. You can also drill holes into the board but note that a new connection should be made to the ground plane from each of the new standoff locations if doing this.

The design reuses the Delta SMP-220DB AC inlet board, and replicates both the original monitor passthrough power relay and fan speed control logic for authentic behaviour.

The 20/24 pin ATX harness is intended to be cut short and looped into the +12V, GND, -12V, +5V, PS_ON and +5VSB vias seen at the top of the new PCB. This is so a soft power inverter can be integrated, and also allows the original modular Mac PSU connector to be fitted in its original location.

Assembly
-
Here are the steps needed to assemble your rebuilt power supply. Note that I'm working with a slightly different pre-release board layout.

<img width="1050" alt="Circuits" src="https://github.com/user-attachments/assets/1e55210a-4ed3-44ca-bfc0-5e1963afb76e" />

Once you have the bare Conversion Board PCB in your hands, decide if you'll be populating the fan circuit and the CRT relay as shown in the key above. Both circuits are optional. If you are not populating the fan control circuit then your fan should be connected to the ATX PCB. The through hole parts should be taken from the original Delta PSU (apart from the fan header), while SMDs should be newly obtained.

To install the AC inlet connector, either re-use the one from the original PSU or purchase a new one.

<img width="950" alt="Circuits2" src="https://github.com/user-attachments/assets/c70cdbd0-3a17-4ce8-b7d6-bd76c96da60c" />

In this corner you'll install the 22-way MiniFit Jr Connector (you can bring this from the old board or purchase new), trimming off the mounting flange on one side in order to make way for a metal standoff. You'll also install a small capacitor and inverter for the soft power circuit.

<img width="701" alt="IMG_0665" src="https://github.com/user-attachments/assets/c1c45b00-9358-4ca9-ad29-e0977ebea4f7" />

Detach this little washer-type part from the original PCB and solder it here.

<img width="1024" height="996" alt="populated" src="https://github.com/user-attachments/assets/64c758e3-02f5-47f8-a480-3315fa9ad85e" />

Now that the Conversion Board is populated you can fit the 4x standoffs. Place the ATX PCB on top and loosely screw it down with just the two standoffs nearest the lower edge.

<img width="4032" height="3024" alt="IMG_0638" src="https://github.com/user-attachments/assets/d00f997d-687a-489b-8b96-7872bb570383" />

From the other side, you can start to trim the wires of your 20/24-pin ATX connector harness to the correct length to connect to the lower PCB. +12V, GND, -12V, +5V, PS_ON and +5VSB are needed; the rest can be shortened and insulated or desoldered as you wish. Hinge the ATX PCB upwards in order to get better access to solder.

You should cut back and insulate (or desolder) any drive connectors you don't need; the remaining ones will feed through the Delta housing circular cutout.

<img width="4032" height="3024" alt="IMG_0663" src="https://github.com/user-attachments/assets/c2c1dd20-d065-4dd2-b228-3387ee5a7ff2" />

Here, all the connections have been successfully made, and the ATX PCB has been fully screwed down. 

<img width="3024" height="4032" alt="IMG_0667" src="https://github.com/user-attachments/assets/9b94c0b1-f417-4170-9aba-3e4f056eab9d" />

Turn the assembly around again, and solder two short wires (live and neutral) from the Conversion Board to the ATX PCB. These should be at least 18AWG and preferably 16AWG.

<img width="4032" height="3024" alt="IMG_0645" src="https://github.com/user-attachments/assets/ae831d0b-ec98-4068-a2d8-ab348d4d42e0" />

The full assembly can now be installed in your Delta housing, and the AC inlet board plugged in to the Conversion Board.

$\color{#FF0000}{IMPORTANT!}$ The two large left-hand heatsinks on the ATX board have a high voltage when the unit is powered up (and for some time after power is disconnected) which will give you a nasty shock if you touch them. Please be extra careful.

<img width="565" height="715" alt="Screenshot 2026-05-12 at 18 22 36" src="https://github.com/user-attachments/assets/401c5e1f-0a63-4bf6-8f0b-08ec8ed00c7d" />

Make sure to insulate the ferrite ring with kapton tape (or similar) so that it does not accidentally short out the exposed solder joints on the back of the inlet board.

<img width="701" height="450" alt="fan-rewire" src="https://github.com/user-attachments/assets/087eb3de-1284-4f06-b8cf-46eeb04f57cc" />

You can re-use the original 120mm fan or install a modern replacement (e.g. Noctua). In my build I opted to re-use the original but it needed a longer cable with a three-pin connector for my Conversion Board's new header. So I peeled back the sticker over the motor to expose the solder points and replace the cable.

<img width="701" alt="Screenshot 2026-05-12 at 18 39 02" src="https://github.com/user-attachments/assets/5cc4250a-8349-4211-ae01-c6a3ee87ad9f" />

The cable was now long enough to reach the new header on the Conversion Board, with plenty of slack for ease of installation.

<img width="1223" height="831" alt="Screenshot 2026-05-12 at 19 10 46" src="https://github.com/user-attachments/assets/c3f87157-fb74-42c7-a63d-7d038d1ff632" />
Here is the PSU fully assembled and ready to use.
