Docker Teamspeak
=================

[CGIT](http://git.zx2c4.com/cgit/) Docker container. Scans and displays every repository under `/git`.

Running the container
----------------------

    docker pull invokr/cgit
    docker run -name cgit -d -p 80:80 -v my/git/repositories:/git invokr/cgit

Optional authentication via htaccess:

    docker run -name cgit -d -p 80:80 -e HTTP_AUTH_USER=user -e HTTP_AUTH_PASSWORD=password -v my/git/repositories:/git invokr/cgit
    
create a git users and add ssh key to it 

    sudo chmod -R 755 /home/git
