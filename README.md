Snaphax: a Python library to use the Snapchat API
==============================================

This library allows you to communicate with Snapchat's servers using their
undocumented HTTP API. It was reverse engineered from the official Android
client (version 1.6)

Adapted from [tlack's PHP library](http://github.com/tlack/snaphax).

Warning
-------

I made Snaphax by reverse engineering the app. It may be extremely buggy or
piss off the Snapchat people. Use at your own risk.

How to use
----------

Pretty simple:

```
    import snaphax
    sh = Snaphax()
    # Login & Get list of snaps
    result = sh.login('username', 'password')
    print result
    # Fetch snap
    image = sh.fetch(result["snaps"][0]["id"])
    # Upload and send snap
    sh.upload(image, sh.MEDIA_IMAGE, ['zjbanks'], time=5)
    # Clear list of recieved snaps
    sh.clear()
```


Future
----------------------

TODO:

- Keep up with tlack's updates! :-)
- Docs
- Figure out the /device call - what's this do? also device_id in /login resp
- Syncing (to mark snaps as seen)
- Friend list maintenance
- Test framework

License
-------

MIT

Credits
-------

Made by Thomas Lackner <[@tlack](http://twitter.com/tlack)> with a lot of help
from [@adamcaudill](http://twitter.com/adamcaudill).  
Ported by [@zbanks](http://github.com/zbanks).
And of course none of this would be possible without the inventiveness of the
[Snapchat](http://snapchat.com) team

