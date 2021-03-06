# media-server-go

[![Build Status](https://travis-ci.com/notedit/media-server-go.svg?branch=master)](https://travis-ci.com/notedit/media-server-go)

WebRTC media server for go



## Functionality

We intend to implement support the following features:

- [x] MP4 multitrack recording support for all WebRTC codecs: H264,VP8,VP9, OPUS and PCMU/A.
- [x] [VP9 SVC](https://tools.ietf.org/html/draft-ietf-payload-vp9-02) layer selection
- [x] Simulcast with temporal layer selection
- [x] [RTP transport wide congestion control](https://tools.ietf.org/html/draft-holmer-rmcat-transport-wide-cc-extensions-01)
- [x] Sender side BitRate estimation
- [ ] [Flex FEC draft 3](https://tools.ietf.org/html/draft-ietf-payload-flexible-fec-scheme-03)
- [x] NACK and RTX support
- [x] [RTCP reduced size] (https://tools.ietf.org/html/rfc5506)
- [x] Bundle
- [x] ICE lite
- [x] [Frame Marking] (https://tools.ietf.org/html/draft-ietf-avtext-framemarking-04)
- [x] [PERC double encryption] (https://tools.ietf.org/html/draft-ietf-perc-double-03)
- [x] Plain RTP broadcasting/streaming
- [ ] [Layer Refresh Request (LRR) RTCP Feedback Message] (https://datatracker.ietf.org/doc/html/draft-ietf-avtext-lrr-04)
- [x] Raw MediaFrame callback
- [x] Raw RTP Data input



## How to use 

[Read the Tutorial](https://github.com/notedit/media-server-go/blob/master/manual.md)


Yon can see the demos from here [Demos](https://github.com/notedit/media-server-go-demo)



## Install 

You should install `libtool` and `autoconf` `automake` before you build 

ubuntu
```
apt install autoconf
apt install libtool
apt install automake
```
macOS
```
brew install libtool
brew install autoconf
brew install automake
```


Your compiler should support c++17, for linux, you should update your gcc/g++ to 7.0+

```
sudo add-apt-repository -y ppa:ubuntu-toolchain-r/test
sudo apt-get update -qq
sudo apt-get install g++-7
sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-7 90
```


Build the native c/c++ code,  it will install `openssl` `libsrtp` `mp4v2` `libmediaserver` into  `/usr/local`

```
git clone --recurse-submodules https://github.com/notedit/media-server-go-native.git  

cd media-server-go-native

make
```

Install mediaserver go lib

```
go get github.com/notedit/media-server-go

```


## Thanks 

 - [Media Server](https://github.com/medooze/media-server)
 - [Media Server for Node.js](https://github.com/medooze/media-server-node)
 - [Murillo](https://github.com/murillo128)






