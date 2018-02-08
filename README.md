# docker-bind-utils
# Deprecated - Use [docker-linux-tools](https://github.com/mapitman/docker-linux-tools) instead!
[![](https://images.microbadger.com/badges/image/mapitman/bind-utils.svg)](https://microbadger.com/images/mapitman/bind-utils "Get your own image badge on microbadger.com") [![](https://images.microbadger.com/badges/version/mapitman/bind-utils.svg)](https://microbadger.com/images/mapitman/bind-utils "Get your own version badge on microbadger.com")

I use this on my Windows system at work to run [BIND](https://www.isc.org/downloads/bind/) utilities like `dig`, `host`, etc.

## Usage

```sh
docker run --rm -it mapitman/bind-utils dig
```

I use functions in my `.bashrc` to make this work seamlessly.

```sh
dig () {
    docker run -it --rm mapitman/bind-utils dig "$@";
}

host () {
    docker run -it --rm mapitman/bind-utils host "$@";
}
```
