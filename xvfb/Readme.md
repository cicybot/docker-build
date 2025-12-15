
    docker build -t xvfb-electron .
    docker run -it -v ./data:/data xvfb-electron bash
    

    xvfb-run electron --no-sandbox --disable-gpu --disable-features=UseDBus --version


    docker logout
    docker login -u USERNAME

    docker tag d3f057a0992b cicybot/xvfb-electron:1.0.1
    docker tag d3f057a0992b cicybot/xvfb-electron:latest  

    docker push cicybot/xvfb-electron:1.0.1
    docker push cicybot/xvfb-electron:latest


    docker run -it -v ./data:/data cicybot/xvfb-electron bash