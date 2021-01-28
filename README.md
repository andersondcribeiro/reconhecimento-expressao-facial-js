<h1>Realtime face expression recognition with JavaScript and face API JS library built on Tensor Flow </h1>


[Code example](https://bit.ly/3iSNKQ2)( need permission to use the camera via browser)

[Face- API-JS Library](https://github.com/justadudewhohacks/face-api.js)



![50575270-f501d080-0dfb-11e9-9676-8f419efdade4](https://user-images.githubusercontent.com/4931735/106178381-74e3fb80-6178-11eb-94ed-c5ec7e3c2b8a.png)


![50575270-f501d080-0dfb-11e9-9676-8f419efdade4](https://user-images.githubusercontent.com/4931735/106178381-74e3fb80-6178-11eb-94ed-c5ec7e3c2b8a.png)



# IMPORTANT: Bug Fixes

## `navigator.getUserMedia`

`navigator.getUserMedia` is now deprecated and is replaced by `navigator.mediaDevices.getUserMedia`. To fix this bug replace all versions of `navigator.getUserMedia` with `navigator.mediaDevices.getUserMedia`

## Low-end Devices Bug

The video eventListener for `play` fires up too early on low-end machines, before the video is fully loaded, which causes errors to pop up from the Face API and terminates the script (tested on Debian [Firefox] and Windows [Chrome, Firefox]). Replaced by `playing` event, which fires up when the media has enough data to start playing.
