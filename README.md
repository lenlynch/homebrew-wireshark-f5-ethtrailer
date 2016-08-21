# homebrew-wireshark-f5-ethtrailer (experimental, optomistic, untested, really)

[![Build 
Status] (https://travis-ci.org/lenlynch/homebrew-wireshark-f5-ethtrailer.svg?branch=master)] (https://travis-ci.org/lenlynch/homebrew-wireshark-f5-ethtrailer) 

Homebrew formula with additional patches for building and installing F5 plugin to process extension data added to pcapng capture files on F5 network gear.

- [F5 Ethtrailer
  Plugin](https://devcentral.f5.com/wiki/advdesignconfig.F5WiresharkPlugin.ashx):
  enable with `--with-f5-ethtrailer`. 
  
  Note:  A DevCentral account is necessary to access these URI.  
  See [[Source] (https://devcentral.f5.com/getting-started)]
  The above URI is documentation provided by F5 Networks, 
  the source for the plugin URI follows:
  [[Source](https://devcentral.f5.com/wiki/GetFile.aspx?Page=AdvDesignConfig.F5WiresharkPlugin&File=wireshark2.plugin.f5ethtrailer.1.11.tar.gz)]

## How to install

If you had previously installed the default homebrew wireshark, you must uninstall
that version first:

```
> brew uninstall wireshark
```

Then proceed with installation based on custom formula:

```bash
> brew tap lenlynch/wireshark-f5-ethtrailer
# There will be a warning regarding overriding existing formula 'wireshark'

> brew options lenlynch/wireshark/wireshark-f5-ethtrailer
# List of available options
# Note that not all combinations are always possible (due to potentially
# conflicting patches).

--with-gtk+3
       	Build the wireshark command with gtk+3
--with-headers
       	Install Wireshark library headers for plug-in development
--with-lua
       	Build with lua support
--with-qt5
       	Build the wireshark command with Qt5 (can be used with or without either GTK option)
--with-f5-ethtrailer
	Build and Install F5 Ethtrailer plugin
				   

> brew install lenlynch/wireshark/wireshark-f5-ethtrailer --with-gtk+3 \
  --with-lua --with-headers --with-qt5 \
  --with-wireshark-f5-ethtrailer
# Compile and install customized wireshark with F5 plugin support
# This is an example, refer to the command above to see the
# available options.
```
