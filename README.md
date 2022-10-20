# Electronics Tools Library for Jitx

This repo contains a set of packages for working in Jitx. These libraries
are intended to help with selecting components, designing circuits,
and checking circuits for the expected results. This library is not
intended to store specific component definitions.

This library attempts to separate out the jitx dependencies from the
pure stanza implementations where possible.

# Build

Make sure you have stanza installed and on your path. Then you can run
the build system with:

```shell
$> stanza build
```

This will compile the package file and place it in the `pkgs` directory. 

# Tests

You will need a version of gcc installed on your path - otherwise the test 
build will fail. I suggest using [mingw-w64](https://www.mingw-w64.org/). 

```shell
$> gcc --version
gcc.exe (x86_64-posix-seh-rev0, Built by MinGW-W64 project) 5.4.0
Copyright (C) 2015 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

$> stanza build etools-test
$> etools-tests.exe
[Test 1] round-places-tests
[PASS]

[Test 2] rounded-log10-test
[PASS]

[Test 3] get-power-of-10-test
[PASS]

[Test 4] E12-test
[PASS]

[Test 5] E24-test
[PASS]

[Test 6] E48-test
[PASS]

[Test 7] E96-test
[PASS]

Tests Finished: 7/7 tests passed. 0 tests skipped. 0 tests failed.

Longest Running Tests:
[PASS] E96-test (998 us)
[PASS] rounded-log10-test (997 us)
[PASS] get-power-of-10-test (0 us)
[PASS] E12-test (0 us)
[PASS] E24-test (0 us)
[PASS] E48-test (0 us)
[PASS] round-places-tests (0 us)
```

