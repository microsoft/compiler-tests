Microsoft compiler-tests
========================

Introduction
------------
This repo includes selected tests from the Microsoft compiler-tests directory. 
The initial focus is on exception handling tests, both for C++EH and SEH, to make it easier to test WinEH implementations for compatibility with the platform.  The expectation is that this set of tests will grow and ultimately be added to the LLVM test-suite.  Opening this as a separate repo is intended as a stop gap as the work to get the LLVM test-suite to run clean on Windows progresses.

Supported Platforms
-------------------
The first round of tests being opened are EH, the bulk of which are SEH tests.  This is naturally Windows specific.  Additionally only the most rudimentary harness is included (runtests.cmd) due to our objective to move these tests into the LLVM harness.

Quick Start
-----------
In the EH sub directory is the C++EH torture test for object destructors.  We have more C++EH tests but there's also a large body of tests out in the community already.  This particular test targets object destructors and is one of the milestone type tests used for validating new EH work.
In the SEH sub directory is a set of SEH tests.  The sehxxxx.c tests are actually factored out sections of the xcpt4u.c test and are included for convenience of implementers as these cut down tests are easier to debug.  

Next Steps
----------
More tests will follow.  If there are particular areas where there are questions please open an issue and we'll see if there are tests that can meet the need.
