# Tiny85_IRremote_ATtinySerialOut
Tiny85 with micronucleaus 2.6, the IR remote testing  


Tiny85, PB4 for IR signal output  


### intall 2 libraries first from Arduino IDE & library manager
Arduino-IRremote
ATtinySerialOut

### open folder of library ATtinySerialOut installed
%USERPROFILE%\Documents\Arduino\libraries\ATtinySerialOut\src

### edit ATtinySerialOut.h to support 16,5MHz for Tiny85 & micronucleaus

```
/%
#if (F_CPU != 1000000) &&  (F_CPU != 8000000) &&  (F_CPU != 16000000)
#error F_CPU value must be 1000000, 8000000 or 16000000
#endif
%/

#if (F_CPU != 1000000) &&  (F_CPU != 8000000) &&  (F_CPU != 16000000) && (F_CPU != 16500000)
#error F_CPU value must be 1000000, 8000000 or 16000000, or 16500000
#endif
```

