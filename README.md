This is heavily based off of https://github.com/DemonTPx/steelseries-arctis-5-pulseaudio-profile.
The Arctis 7 has similar issues to the Arctis 5.

# SteelSeries Arctis 7 pulseaudio profile

The SteelSeries Arctis 7 is a gaming headset which has two stereo audio outputs. One for voice chat and one for the rest of the sound. It can be mixed between with a physical knob.

By default, pulseaudio only enables the voice chat output. This profile enables the second (game) output and the udev rule makes sure this profile is used when plugging in the device.

## Installing
### From source

Install from by copying the following files:

- `steelseries-arctis-7-output-game.conf` and `steelseries-arctis-7-output-chat.conf` to `/usr/share/pulseaudio/alsa-mixer/paths/`
- `steelseries-arctis-7-usb-audio.conf` to `/usr/share/pulseaudio/alsa-mixer/profile-sets/`
- `91-pulseaudio-steelseries-arctis-7.rules` to `/lib/udev/rules.d/`

Restart pulseaudio:

    pulseaudio -k
    pulseaudio --start

After that, plug in the device to see if it works.
