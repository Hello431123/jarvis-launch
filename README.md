# jarvis-launch

A tiny static redirect helper for a private, self-hosted assistant whose web address changes every time it starts.

**It contains no secrets, no addresses and no personal information.** It is one HTML file with inline JavaScript:

- It only ever opens addresses of the form `https://<random>.trycloudflare.com`.
- A device the owner chose to trust keeps a random token and a check key in *this browser's* storage (put there by the private server through the URL #fragment, which browsers never send to any server).
- It hands the token to an address only if that address carries a valid signature made with that key, so a link to anyone else's address gets nothing.
- **Forget this device** clears what it kept.

The private server it points to is not here and is never published. Without the owner's pairing code and PIN, or a trusted device, that server shows only a locked page.
