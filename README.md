# CENO Windows installer

## How to use

Assumes a clone of the [ceno repository](https://github.com/equalitie/ceno) in the `ceno` directory.

### Current CENO 0.5.0 instructions

1. Install CENO.
2. Launch Freenet (if not already done at the end of the installer by checking "Launch CENO" on the last page.)
3. Allow Freenet through the firewall if prompted.
4. Launch the client: Go to the Freenet installation directory (one way to do this is to open the download directory with the Freenet tray and go up to its parent), go to client, and run client.exe.
5. Allow the CENO client through the firewall if prompted.
6. Start Firefox - either with the custom profile in `ceno\browser-profiles\firefox` - or set FTP, HTTP, HTTPS, and SOCKS proxies to 127.0.0.1 port 3090.
7. Add the CENO plugin - Menu > Add-ons > Gear > Install Add-on From File > `ceno\browser-extension-builds\cenorouter@equalit.ie-1.0.0.xpi`
8. Browse to a website! Requesting a page will take around an hour.

### Instructions given a CENO tray app that launches Freenet and starts Firefox with the custom profile (not implemented)

1. Install CENO.
2. Launch CENO (if not already done at the end of the installer by checking "Launch CENO" on the last page.)
3. Allow the CENO client / Freenet through the firewall if prompted.
4. Add the CENO plugin - Menu > Add-ons > Gear > Install Add-on From File > `ceno\browser-extension-builds\cenorouter@equalit.ie-1.0.0.xpi`
5. Browse to a website! Requesting a page will take around an hour.

## Development

Because this is Windows software it is okay for a file to not have an ending newline. If you edit
such a file please keep it that way.

So that they can be uploaded to Transifex there are two encodings of the
localization files. UTF8 as required by Transifex, and usually-ANSI, as required
by InnoSetup. To convert between them see
[convert-inno-setup](https://github.com/freenet/scripts/blob/master/convert-inno-setup).

--
## How to build
* Download InnoSetup from http://www.jrsoftware.org/download.php/is-unicode.exe (see http://www.jrsoftware.org/isdl.php)

### On Linux (with wine)
* Install InnoSetup : wine is-unicode.exe /SILENT
* TODO: How to build [wintray](https://github.com/freenet/wintray) on Linux?
* Build the Setup :  wine "C:\Program Files (x86)\Inno Setup 5\ISCC.exe" "FreenetInstall_InnoSetup.iss"
* See Output folder

### On Windows
* Install InnoSetup
* Build [wintray](https://github.com/freenet/wintray) and copy it to install_node\FreenetTray.exe
* Build the Setup : ISCC.exe "FreenetInstall_InnoSetup.iss"
* See Output folder