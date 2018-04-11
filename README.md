# Test issues for LIBC broken tests

    This document contains the analysis of various tests in libc tests.broken that fail.

* One test in tests.all is not classified. Since the test fails moved it to tests.broken. 

           ../../3rdparty/musl/libc-test/src/common/runtest.c

  This test was throwing undefined reference error while compiling. 
  
### Error :

       openenclave/tests/libc/enc/../../../3rdparty/musl/libc-test/src/common/runtest.c:21: undefined reference to `fork'
       openenclave/tests/libc/enc/../../../3rdparty/musl/libc-test/src/common/runtest.c:28: undefined reference to `execv'
       openenclave/tests/libc/enc/../../../3rdparty/musl/libc-test/src/common/runtest.c:54: undefined reference to `optarg'
       openenclave/tests/libc/enc/../../../3rdparty/musl/libc-test/src/common/runtest.c:51: undefined reference to `getopt'
       openenclave/tests/libc/enc/../../../3rdparty/musl/libc-test/src/common/runtest.c:63: undefined reference to `optind'
       openenclave/tests/libc/enc/../../../3rdparty/musl/libc-test/src/common/runtest.c:66: undefined reference to `sigemptyset'
       openenclave/tests/libc/enc/../../../3rdparty/musl/libc-test/src/common/runtest.c:67: undefined reference to `sigaddset'
       openenclave/tests/libc/enc/../../../3rdparty/musl/libc-test/src/common/runtest.c:68: undefined reference to `sigprocmask'
       openenclave/tests/libc/enc/../../../3rdparty/musl/libc-test/src/common/runtest.c:69: undefined reference to `signal'
       openenclave/tests/libc/enc/../../../3rdparty/musl/libc-test/src/common/runtest.c:76: undefined reference to `sigtimedwait'
       openenclave/tests/libc/enc/../../../3rdparty/musl/libc-test/src/common/runtest.c:81: undefined reference to `kill'
       openenclave/tests/libc/enc/../../../3rdparty/musl/libc-test/src/common/runtest.c:84: undefined reference to `waitpid'
       openenclave/tests/libc/enc/../../../3rdparty/musl/libc-test/src/common/runtest.c:96: undefined reference to `strsignal'



