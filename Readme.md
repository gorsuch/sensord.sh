# sensord.sh

A simple http sensor written in `bash`, leveraging `curl`.

It reads data from `./sites.txt` and renders output like so:

```bash
$ ./sensord 
app=sensord location=dev measure=sensor.dev.19b8b5836ff2705559dcfb12d3694bcab42ad9e5.latency value=0.218 timestamp=1356808274
app=sensord location=dev measure=sensor.dev.19b8b5836ff2705559dcfb12d3694bcab42ad9e5.availability value=100 timestamp=1356808274
```

`sites.txt` consists of urls, one per line.  In the output, all urls are run through `sha1sum` first so we have unique names for measurement.
