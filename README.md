# pyqt5_stream_rtsp_example

Example to display a RTSP stream in a Qt5 desktop application with libVLC. This example was tested in Ubuntu 16.04.

## Install

`sudo apt install vlc`
`pip install python-vlc`

or (if you are using python3):

`pip3 install python-vlc`

## Run

- Test VLC streaming of your local webcam:

`vlc v4l2:// :v4l2-dev=/dev/video0 :v4l2-width=640 :v4l2-height=480 --sout="#transcode{vcodec=h264,vb=200,scale=1,acodec=mp4a,ab=128,channels=2,samplerate=44100}:rtp{mux=ts,sdp=rtsp://127.0.0.1:8554/live.sdp}" -I dummy`

- Execute the Qt window:

`python main.py`
