# P2P Image share

This is a super simple P2P image sharing using WebRTC. I wrote this page under one evening using my poor JS skills and ChatGPT. So how does it work?

1. On the receiving side you open the page which will display a QR code.
2. On the sending you open the page by scanning the code from the sending side. The QR code contains the [PeerJS](https://peerjs.com/) peer ID.
3. On the send side the only thing displayed on the page is the file input. You chose a file to send and it will be sent over WebRTC data channel to the receiving side.
4. The receving side will replace the QR code with the image. That's it.

## Why is it useful?

Someone asked me how can you send an image from a phone to a computer without having to upload it anywhere and without being logged in to any accounts on either of the devices. I didn't have a good answer so I wrote this page. What's fascinating is that pre ChatGPT I wouldn't bother at all. I mean I could get exactly the same result but definitely not in an hour or so that I spent on this page.

## Why you shouldn't use this page.

While the data sent between the peers is not uploaded to any server it's currently not encrypted in transit, which means anyone between the peers can intercept it. Adding a simple encryption key to the QR code would probably be pretty straight forward, but it's currently out of scope of this experiment 🙃.
