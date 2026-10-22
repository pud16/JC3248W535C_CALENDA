# JC3248W535C Calendar v3

Built using the **verified diagnostic v2 display + touch pins** and **the exact working PlatformIO QIO/80MHz/QIO_OPI settings** provided after a real device test.

## Functions
- Russian-language month calendar; touchscreen month navigation.
- Large clock with seconds and Russian date.
- 25/5-minute focus timer; start/pause/reset.
- Wi-Fi configuration access point and UTC time-zone setting; NTP sync.
- Four touchscreen tabs (calendar / clock / timer / network).

## First start
No Wi-Fi credentials: connect a phone or computer to `CALENDAR-SETUP`, password `calendar123`. Open `http://192.168.4.1`; enter home Wi-Fi credentials. This is a local setup AP; avoid using this default password on an untrusted network. In the Network tab set UTC offset (default +3). Time/date appears after internet NTP sync. No internal real-time clock battery is assumed.

**This build intentionally does not fetch weather yet.** This is a functional UI verification build. Displays in 320x480 portrait mode, exactly as the confirmed working diagnostic v2.

## Building
Upload the *contents* of this folder to the root of your GitHub repo. Actions > Build JC3248W535C Calendar v3 > Run workflow. Download the ZIP artifact and extract `JC3248W535C_CALENDAR_V3_fullflash.bin`.

Flash the combined binary at **0x0**, as with the diagnostic image. Keep a copy of your working v2 diagnostic firmware before testing. Confirm hardware display/touch in this v3 first. The compilation has NOT been run or verified in this environment; GitHub Actions will report any build issues.
