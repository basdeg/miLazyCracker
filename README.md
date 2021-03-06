# miLazyCracker
Mifare Classic Plus - Hardnested Attack Implementation for LibNFC USB readers (SCL3711, ASK LoGO, etc)

Installation:
```bash
./miLazyCrackerFreshInstall.sh
```

Extra steps to make it work:
```bash
modprobe -r pn533_usb
modprobe -r pn533
nano /etc/modprobe.d/blacklist-libnfc.conf
```

Make sure the file contains and save it
```
blacklist nfc
blacklist pn533
blacklist pn533_usb
```

Now unplug the RFID reader, and connect it again (IMPORTANT STEP) 

Youre done ;) 



__

Usage example: place a tag and enjoy
```bash
mkdir mydumps
cd mydumps
miLazyCracker
```

This tool is comprised of work from:
-  Aram Verstegen (https://github.com/aczid/crypto1_bs) 

-  Carlo Meijer and Roel Verdult: (http://www.cs.ru.nl/~rverdult/Ciphertext-only_Cryptanalysis_on_Hardened_Mifare_Classic_Cards-CCS_2015.pdf)

-  Iceman Proxmark Branch: https://github.com/iceman1001/proxmark

-  Piwi Proxmark Branch - https://github.com/pwpiwi/proxmark3/tree/hard_nested

-  Blahpost Solver

-  MFOC - https://github.com/nfc-tools/mfoc

-  MFCUK - https://github.com/nfc-tools/mfcuk

