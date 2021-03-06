# krpc
    Kodi jsonRPC :: wrapper to manipulate Kodi's jsonRPC
    Author: Spencer Butler <github@crooked.app>

## History
I started this because I wanted a way to update the libraries, on the command line, after adding new content.
Well, I kept adding stuff and things and here we are. Feel free to do foo with this.

## Usage
cp krpc.cfg to ~/.krpc.cfg with settings germane to your environment


     usage: ./krpc [Option] <param>
     
         Requires: curl jq
     
         Player Options: (media type is autodetected)
         -seek --seek <seconds>       negatives rewind :: values < 60 start at that sec
         -sf --seek-forward           seek small forward
         -sb --seek-backward          seek small backward
         -gn --goto-next              goto next item in playlist
         -gp --goto-previous          goto previous item in playlist
         -pi --player-info            query current playing media
         -p --pause                   pause the current media source
         -po --player-open            currently [mostly] broken
         -pm --party-mode             start new music partymode
         -v --volume <increment|decrement> or <0..100>
     
         Library Options:
         -as --audio-scan             scan the audio library for new content
         -ac --audio-clean            clean the audio library
         -vs --video-scan             scan the video library for new content
         -vc --video-clean            clean the video library
     
         GUI Options:
         -gg --go-gui <action>       one of the following <action>
                                     Back         Info   ShowCodec
                                     ContextMenu  Left   ShowOSD
                                     Down         Right  ShowPlayerProcessInfo
                                     Select       Up     ExecuteAction
                                     Home         SendText
     
         Debug Options:
         -ad --ad-hoc <method> <key> <value>
         -ff --free-form <valid json query>
         -m --methods                 see valid methods
         -i --introspect <method>     debug stuff
