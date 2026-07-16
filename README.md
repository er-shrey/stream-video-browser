# Stream Video Browser

A Flask + OpenCV webcam streamer with built-in motion detection. It captures frames from a webcam, detects motion against a running background model, and streams the annotated live feed as MJPEG to any browser on the network.

## Tech Stack

- Python
- [Flask](https://flask.palletsprojects.com/) 1.1.2
- [OpenCV](https://opencv.org/) (`opencv-python`)
- [imutils](https://github.com/PyImageSearch/imutils)
- NumPy

## Prerequisites

- Python 3 (a version compatible with the pinned dependencies, e.g. Python 3.6–3.8)
- pip
- A webcam accessible to the machine running the script

## Installation

```bash
git clone https://github.com/er-shrey/stream-video-browser.git
cd stream-video-browser

python3 -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate

pip install -r requirements.txt
```

## Running it

```bash
python stream.py -i <SERVER_IP> -p <SERVER_PORT>
```

Then open `http://<SERVER_IP>:<SERVER_PORT>/` in a browser to view the live, motion-annotated feed.

### Options

```bash
python stream.py --help
```

- `-h`, `--help` — show help
- `-i`, `--ip` — server IP to bind to
- `-p`, `--port` — server port to bind to
- `-f`, `--frame-count` — number of frames used to construct the background model for motion detection

## Project structure

- `stream.py` — Flask app: captures video, runs motion detection, streams MJPEG output
- `pyimagesearch/` — `SingleMotionDetector` implementation used by `stream.py`
- `templates/` — HTML template for the browser view
- `images/` — example/preview images
