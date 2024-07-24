``Run the file``

To start the program, you just open a terminal with the location is the root of project folder, and you can input prompt like this :

``` shell
go run . --domain [domain to check] --port [port to check]
```

You can fill ``[domain to check]`` with a real domain like ``facebook.com``, ``google.com``, ``youtube.com``, etc.

But the flag ``[port to check]`` is not mandatory. Don't worry, you can set it blank, by default it will be replaced to ``80``.

The clear example without ``port``:

```shell
go run . --domain youtube.com
```

The clear example with ``port``:

```shell
go run . --domain facebook.com --port 5090
```

If the domain is reachable, this program will show the response result like this :
```shell
[UP] youtube.com is reachable.
From : [result of local address]
To   : [result of remote address]
```

But if the domain is unreachable, the program will show you the result like this :
```shell
[DOWN] randomurl12930.com is unreachable. 
Error: dial tcp: lookup randomurl12930.com: getaddrinfow: A non-recoverable error occurred during a database lookup.
```