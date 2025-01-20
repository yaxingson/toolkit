# WebRTC

## Intro

> WebRTC（Web Real-Time Communication）

[WebRTC specification architecture](./webrtc.png)

Communication principle:

- Media negotiation: The process by which two communication parties exchange information through the _SDP_ protocol
- Network negotiation: Exchange network information through _STUN_ and _TURN_ protocol servers

Signaling server

APIs:

- `navigator.mediaDevices.getUserMedia`
- `window.RTCPeerConnection`
- `window.WebSocket`

## Implementation

### Install coturn

```sh
sudo yum install openssl-devel
sudo yum install libevent-devel

git clone https://github.com/coturn/coturn

cd coturn
./configure
make
sudo make install

```

### Media Stream

```js
navigator.mediaDevices
  .getUserMedia({ audio:true, video:true })
  .then(function (stream) {
    const el = document.getElementById('')
    el.srcObject = stream
  })
  .catch(function (err) {
    console.error(`error: ${err}`)
  });


```



