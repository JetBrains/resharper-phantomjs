# resharper-phantomjs

An extension for ReSharper 8.1 that bundles [PhantomJS](http://phantomjs.org) and automatically configures ReSharper to use it when running JavaScript tests. You can install the extension from ReSharper's Extension Manager dialog.

# More info

ReSharper 7 introduced support for [running JavaScript unit tests](http://blogs.jetbrains.com/dotnet/2012/07/unit-testing-improvements-in-resharper-7/), with support for [Jasmine](http://pivotal.github.io/jasmine/) and [QUnit](http://qunitjs.com/). By default, tests are run in the system browser, and reported in the normal ReSharper test runner. This is inconvenient, since it opens a new window on each run, and is unable to close it at the end of the run.

However, ReSharper 7 also introduced the option to run tests with PhantomJS, which is a "headless" web browser, based on WebKit. This is a browser with no user interface, and since it doesn't need to draw anything - it's FAST. The only downside is that you need to download and install PhantomJS yourself, and point ReSharper to the executable.

This extension automates the process. It bundles the current version of PhantomJS (1.9.2) into the extension, and includes a settings file that automatically configures ReSharper to use this bundled version.

# Requirements

This extension requires ReSharper 8.1.