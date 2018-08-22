# krpc
    Kodi jsonRPC :: wrapper to manipulate Kodi's jsonRPC
    Author: Spencer Butler <spencerunderground@gmail.com>

## History
I started this because I wanted a way to update the libraries, on the command line, after adding new content.
Well, I kept adding stuff and things and here we are. Feel free to do foo with this.

## Usage

    usage: ./krpc [Option] <param>
 
        Requires: curl jq
 
        Player Options: (media type is autodetected)
        -seek --seek <seconds>                negatives rewind :: values < 60 start at that sec
        -sf --seek-forward            seek small forward
        -sb --seek-backward           seek small backward
        -goto --goto <next|previous>  goto next/previous in playlist (-gn -gp)
        -gn --goto-next                       goto next item in playlist
        -gp --goto-previous           goto previous item in playlist
        -pi --player-info             query current playing media
        -p --pause                    pause the current media source
        -v --volume <increment|decrement> or <0..100>
 
        Library Options:
        -as --audio-scan              scan the audio library for new content
        -ac --audio-clean             clean the audio library
        -vs --video-scan              scan the video library for new content
        -vc --video-clean             clean the video library
 
        GUI Options:
        -gg --go-gui <action>                one of the following <action>'s
                                     Back         Info   ShowCodec
                                     ContextMenu  Left   ShowOSD
                                     Down         Right  ShowPlayerProcessInfo
                                     Select       Up     ExecuteAction
                                     Home         SendText
 
        Debug Options:
        -ad --ad-hoc <method> <key> <value>
        -m --methods                  see valid methods
        -i --introspect <method>      debug stuff
