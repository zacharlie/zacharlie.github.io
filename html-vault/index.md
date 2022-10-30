# The HTML Vault

Many (far more than I'll care to admit) moons ago... I figured that stashing sensitive data in an HTML page that is encrypted and decrypted with clientside javascript may be useful. So this tool simply embeds encrypted html content into another html page with a structure that is specifically designed to decrypt the page content and load it when needed.

- [Encrypt html content](./index.html)
- [Example without a password](./samples/nopass.html)
- [Example with a password prompt and the password 123](./samples/123.html)
- [Example with the password qwerty](./samples/qwerty.html)

This is not designed to replace something like keepass, bitwarden, or other somesuch system that would present a false sense security... and not to provide a CMS or documentation framework with access control and the like.

Rather, the idea would be to provide a simple and easy way for folk to provide limited password protected access to specific files which may include rich interactive (client side) content.

Using [GPG](https://gpgtools.org/) or another encryption tool is going to give better protection to anything a vanilla html app will.

Specific use cases this might come in handy include:

- Short lived data protection with generic keyless encryption
- Sensitive files stored on a shared file server without additional security measures (ew)
- Handing over "readme" style instructions which might include sensitive information

I found these old files and wondered if it was useful at all anyway before publishing. To my surprise I found much fresher implementations of the same concept:

- https://robinmoisson.github.io/staticrypt/
- https://github.com/MaxLaumeister/pagecrypt

All of these implementations (at least superficially) have very similar design - which is a sign to me that my implementation is not terrible (if not ideal).

One thing that I reckon sets my old version apart was the inclusion of identicons - without access to the file contents it might be difficult to figure out which password unlocks a files contents. Identicons graphically represent a hash of the file content and a screenshot can be stored in a password manager to help with password management.

Key features I would consider missing are saving the decrypted output, and the inclusion of a timeout mechanism that locks the page after inactivity. Fairly simple considering all it takes is a page refresh, although keeping state for more modern content could be trickier. Either way I haven't looked at this in ages so I probably won't be adding it anytime soon.

This was a toy very simply stitched together. Realistically a dedicated app for file conversion and encryption makes more sense, although the resulting html structure probably wouldn't change much.

> **STATING THE OBVIOUS**: This is not a security system and was made for fun years ago with no maintenance since. It *WILL* eat your homework.
