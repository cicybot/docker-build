
    docker build -t xvfb .
    docker run -it -v ./data:/data xvfb bash
    

    xvfb-run electron --no-sandbox --disable-gpu --disable-features=UseDBus --version
