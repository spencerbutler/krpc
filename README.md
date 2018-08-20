# krpc
Kodi jsonRPC :: wrapper to manipulate Kodi's jsonRPC

## History 
I started this because I wanted a way to update the libraries, on the command line, after adding new content.
Well, I kept adding stuff and things and here we are. Feel free to do foo with this.

usage: ./krpc [Option] param

        Requires: curl jq python

        Player Options: (media type is autodetected)
        -seek --seek <seconds>           negative values rewind :: values < 60 start at that position
        -sf --seek-forward               seek small forward
        -sb --seek-backward              seek small backward
        -goto --goto <next|previous>     goto next/previous in playlist
        -gn --goto-next                  goto next item in playlist
        -gp --goto-previous              goto previous item in playlist
        -pi --player-info                query current playing media
        -p --pause                       pause the current media source
        -v --volume <increment | decrement> or <0..100>

        Library Options:
        -as --audio-scan                 scan the audio library for new content
        -ac --audio-clean                clean the audio library 
        -vs --video-scan                 scan the video library for new content
        -vc --video-clean                clean the video library
 
        GUI Options:
        -gg --go-gui <Back | ContextMenu | Down | ExecuteAction | Home | Info | Left | Right | Select | SendText | ShowCodec | ShowOSD | ShowPlayerProcessInfo | Up>

        Debug Options:
        -ad --ad-hoc <method> <key> <value>
        -m --methods                     see valid methods
        -i --introspect <method>         debug stuff
