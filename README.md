# pynvtx
Add python source code annotations to nvprof trace file

## Running

  nvprof pynvtx.py my-script.py
  
  pynvtx --help

## Docker

pynvtx can be added to a docker image with the following snippet.
This will place pynvtx into `/opt/openvprof` and make it executable.

```docker
# install pynvtx.py
RUN mkdir -p /opt/openvprof
ADD https://raw.githubusercontent.com/cwpearson/pynvtx/pynvtx.py /opt/openvprof/pynvtx.py
RUN chmod ugo+rx /opt/openvprof/pynvtx.py
ENV PATH /opt/openvprof:$PATH
```

# Acknowedgement

This script was initially developed while I was an intern at IBM T. J. Watson Research during fall 2018.
