# ECE 568
# 02 Hw2

## Caching Proxy Server

Developer: Chelsea (Jiyuan) Lyu - jl1230,
           Jingxuan Li - jl1226
           
This project involves the creation of an HTTP proxy server in C++. The proxy forwards requests to an origin server on behalf of a client, caches responses, and serves cached copies of resources when appropriate.

## Features

- **Request Handling**: Supports GET, POST, and CONNECT methods. Other HTTP methods may be handled optionally.
- **Caching**: Implements caching for 200-OK responses to GET requests, with expiration and re-validation policies.
- **Concurrency**: Handles multiple concurrent requests using multiple threads. Implements thread safety for shared cache access.
- **Logging**: Generates detailed logs for each request, including request handling, cache status, and errors, saved in `/var/log/erss/proxy.log`.

## Technical Details

- **Programming Language**: C++
- **Key Concepts**: Object-Oriented Design, RAII, Exceptions.
- **Robustness**: Handles external failures gracefully and ensures robustness against malformed requests and responses.



### Docker Set up

This project can be run in docker:

1. Make sure is under the `02_hw2/docker-deploy` directory

2. Run `chmod +x src/run.sh`

3. Run `sudo docker-compose down --remove-orphans`

4. Run `sudo docker-compose up --build`

### `Requirements.xlsx` and `danger_log.txt`

These two files is located in the same directory with this README file.

### `proxy.log`

After the server is running in docker, the log file of server `proxy.log` can be found inside `02_hw2/docker-deploy/logs`.

### Codes

All the codes and development could be found in `02_hw2/docker-deploy/src`.

### Test Program

The `testRequest.cpp` and `testResponse.cpp` are used for testing. 
