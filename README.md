# [Bazel](https://bazel.build)

*{Fast, Correct} - Choose two*

Bazel with proxy.

  The bazel now, can not work under a network with proxy, so I
  make this project and add a new package download method, 
  which using simple wget command.

  Please confirm your machine has wget installed

  * **Install bazel**:<br>
  
    download code:<br>
    git clone https://github.com/ixuexi/bazel.git<br>

    build bazel:<br>
    bazel build //src:bazel
    
  * **Setup proxy env**:<br>
  
    declare proxy env by:<br>
    export http_proxy=http://proxy.example.com:8080<br>
    export https_proxy=http://proxy.example.com:8080<br>
    export ftp_proxy=http://proxy.example.com:8080<br>
    
    or edit /etc/wgetrc file and append the lines:<br>
    http_proxy=http://proxy.example.com:8080<br>
    https_proxy=http://proxy.example.com:8080<br>
    ftp_proxy=http://proxy.example.com:8080<br>

    if the proxy need auth, the url will be:<br>
    http://username:password@proxy.example.com:8080

  * **Setup wget (optional)**:
  
    you can change the wget command with absolute path by:<br>
    export BAZEL_WGET=/home/somedir/wget<br>
    (default: wget)

    you can change the wget options by:<br>
    export BAZEL_WGET_OPT="--timeout=30"<br>
    (default is: --tries=3 --timeout=15 --no-check-certificate)

  * **Changlog**:
    - bazel clear the env http_proxy by default, just remove it
    - try download by default method, if error, then use wget instead
    - add a wget download method, which direct use wget command on your machine
    
--------

## Getting Started

  * [Install Bazel](https://docs.bazel.build/install.html)
  * [Get started with Bazel](https://docs.bazel.build/getting-started.html)
  * Follow our tutorials:

    - [Build C++](https://docs.bazel.build/tutorial/cpp.html)
    - [Build Java](https://docs.bazel.build/tutorial/java.html)
    - [Android and iOS](https://docs.bazel.build/tutorial/app.html)

## Documentation

  * [Bazel command line](https://docs.bazel.build/user-manual.html)
  * [Rule reference](https://docs.bazel.build/be/overview.html)
  * [Use the query command](https://docs.bazel.build/query.html)
  * [Extend Bazel](https://docs.bazel.build/skylark/index.html)
  * [Write tests](https://docs.bazel.build/test-encyclopedia.html)
  * [Roadmap](https://bazel.build/roadmap.html)
  * [Who is using Bazel?](https://github.com/bazelbuild/bazel/wiki/Bazel-Users)

## Contributing to Bazel

See [CONTRIBUTING.md](CONTRIBUTING.md)

[![Build Status](http://ci.bazel.io/buildStatus/icon?job=bazel-tests)](http://ci.bazel.io/job/bazel-tests)

Bazel is released in 'Beta'.
See the [product roadmap](https://bazel.build/roadmap.html) to learn about the
path toward a stable 1.0 release.
