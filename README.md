# Motion sensing Webcam Streaming

This project can be used to stream webcam live feed directly to the browser, in short on a network.

That live feed can be accessed using the browser.

![alt text](/images/example.png)


#### Installing Dependencies
`pip install -r requirements.txt`

> You can use virtualenv to install dependencies


#### Starting Streaming
`
python stream.py  -i <SERVER_IP> -p <SERVER_PORT>
`

#### Help Options

`python stream.py <option>`
You have following options for streaming help
- -h or --help: for help
- -i or --ip: for server IP
- -p or --port: for server port
- -f or --frame-count: Number of frames can be used to construct background model

