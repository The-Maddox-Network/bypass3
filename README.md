# TMN Bypass 3.0
A web proxy for use in combating web filters based on [Alloy](https://github.com/titaniumnetwork-dev/alloy)
The primary difference is Bypass 3.0 uses a whitelist system so only domains that are specified will work. If you prefer a more general proxy use Alloy.

## Running locally

```sh
git clone https://github.com/The-Maddox-Network/bypass3.git
cd bypass3
node server.js
```


## Options in config.json
```json
{
    "port": "80",
    "ssl": false,
    "prefix": "/web/",
    "localAddresses": [],
    "allowedHostnames": []
}
```

`"port": "80"` = Sets HTTP server port of web proxy.

`"ssl": "false"` = Sets HTTP server SSL.

`"prefix": "/web/"` = Sets the overall prefix of the web proxy.

`"localAddresses": [ "0.0.0.0" ]` = Allows you to choose which IP to make the request from. If there are multiple IP's then the IP chosen will be randomized.

`"allowedHostnames": [ "example.org", "example.com" ]` = If the hostname of the proxy URL matches any of the URL hostnames listed in the array, the request to the server will be allowed. If this is left blank all pages will be blocked.
