# ESPHome IEC 62056-21 Component+
This component is based on "Aquaticus ESPHome IEC 62056-21 Component" (https://github.com/aquaticus/esphome-iec62056), and resolves timeout issues for some meters with the bidirectional 'Mode C' of the IEC 62056-21 standard.

The additions of this project are based and tested on a single meter that uses namely Mode C using a wired connection.

**Additional Parameters:**  
```yaml
iec62056:
  initial_baud_rate: 9600
  fixed_baud_rate: True
``` 
- (Optional) initial_baud_rate[Default = 300]:  
    - This is is the speed which is used for the first message to the meter.
    - For Mode C of the IEC 62056-21 standard, this is usually done by a baud rate of 300.
    - But some meters seems to run "out of specs"  

- (Optional) fixed_baud_rate[Default = False]:  
    - This Parameter disables lowering the transmission speed after a failed transmission.
    - Only useful, if the meter expects a specific speed.


**Aquaticus' Documentation:** https://aquaticus.info/iec62056.html
