# NX BUG REPORT

Required package error occurred when execute "nx run" script in nx >= 18 version.

Nx version is lower than 18 (ex: 17.3.1), it works normally

# Environment

- node : 20.11.0
- nx : 18.0.4
- yarn : 4.1.0

# Reproduce

1. clone this project

`git clone https://github.com/ChoSeoHwan/nx-bug-report-0.git`


2. preparation step

`yarn install`


3. reproduce error case

`yarn nx run reproduce:build`


# Current

```shell
Error: Your application tried to access chalk, but it isn\'t declared in your dependencies; this makes the require call ambiguous and unsound.

Required package: chalk
Required by: C:\Projects\NX-BUG~1\YARN~1\UNPLUG~1\NX-VIR~2\NODE_M~1\nx\src\utils\

Require stack:
- C:\Projects\NX-BUG~1\YARN~1\UNPLUG~1\NX-VIR~2\NODE_M~1\nx\src\utils\logger.js
- C:\Projects\NX-BUG~1\YARN~1\UNPLUG~1\NX-VIR~2\NODE_M~1\nx\src\utils\params.js
- C:\Projects\NX-BUG~1\YARN~1\UNPLUG~1\NX-VIR~2\NODE_M~1\nx\src\command-line\run\run.js
# ...
```


# Expect

run executor normally
