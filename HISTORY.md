## 1.0.1 (2011-12-18)

* Workaround for [CLJ-885](http://dev.clojure.org/jira/browse/CLJ-885)

## 1.0.0 (2011-12-11)

* Multipart parameters with same name correctly create vector of values
* Fixed exception when resource-response is passed a directory
* wrap-reload middleware changed to act like wrap-reload-modified
* wrap-keyword-params ignores parameter names that cannot be keywords
* wrap-keyword-params can be safely applied multiple times
* Removed ring.middleware.static
* Servlet outputstream no longer explicitly closed and flushed
* Downgraded Jetty from 6.1.26 to 6.1.25 to solve socket issue
* Jetty SSL adapter respects the :host option
* Cookies can be set as http-only
* Fixed wrap-params for non-UTF8-encoded POST requests
* Fixed wrap-multipart-params bug that occurs in Clojure 1.3.0
* Better error reporting on invalid cookie attributes in wrap-cookies

## 0.3.11 (2011-07-14)

* Multipart parameter storage backends (temp-file and byte-array)
* Added redirect-after-post utility function
* Character encoding of response set from content type

## 0.3.10 (2011-06-28)

* Updated Hiccup to 0.3.6 for Clojure 1.3.0 compatibility

## 0.3.9 (2011-06-26)

* wrap-params no longer excepts on invalid urlencoded query string
* ring.util.servlet accepts multiple headers of the same name

## 0.3.8 (2011-04-23)

* resource-response returns File object when possible
* Added resource middleware
* Stacktrace middleware displays causes (nested exceptions)
* Bug fixes and refactor of stacktrace middleware

## 0.3.7 (2011-03-05)

* Lint middleware recognises ISeq as valid response body
* Added ring.util.mime-types namespace
* Added content-type middleware

## 0.3.6 (2011-02-16)

* Session and flash middleware handle nils without excepting
* Cookie session store compares HMAC with constant-time function

## 0.3.5 (2010-11-27)

* Context classloader now used for resource responses
* Removed HttpCore adapter from repository
* InputStream response body guaranteed to close
* Updated Jetty dependencies to 6.1.26

## 0.3.4 (2010-11-16)

* wrap-cookies no longer overwrites existing Set-Cookie header
* String response bodies no longer have extra newline

## 0.3.3 (2010-10-31)

* Added console logging for ring.handler.dump and ring.middleware.stacktrace
* Removed runtime dependency on clojure.contrib

## 0.3.2 (2010-10-11)

* Added nested-params middleware

## 0.3.1 (2010-09-26)

* Fixed multipart string encoding bug
* Memory sessions can now take a user-defined atom as an argument
* file-info middleware date checking improved
* Added option map to file middleware
* Jetty adapter :configurator option can now set Jetty handlers

## 0.3.0 (2010-09-19)

* Updated Clojure and Clojure-Contrib version to 1.2.0

## 0.2.6 (2010-09-09)

* Fixed non-string param values in keyword params middleware

## 0.2.5 (2010-07-06)

* Hopefully the last flash middleware fix we'll need
* Added ring.util.response/resource-response function

## 0.2.4 (2010-07-04)

* Fixed race condition in file-info middleware date parsing
* Forced US locale for file-info middleware date parsing
* Fixed NPE in multipart-params middleware when field is nil
* Fixed another flash middleware bug that was wiping out session data

## 0.2.3 (2010-06-17)

* Code updated to be more Clojure 1.2 compatible
* Fixed bug in r.m.flash that was wiping out the session
* Added If-Modified-Since support to r.m.file-info
* Added ring.util.response/header
* Added :root key to r.m.session as a shortcut to cookie path attribute
* Updated ring-devel to use Hiccup instead of clj-html
* Session cookie attributes can now be set by adding a :session-cookie-attrs key to the response.

## 0.2.2 (2010-05-16)

* Introduce middleware for session flash
* Cookie middleware made to work for browsers that don't follow cookie RFC (which is most of them)

## 0.2.1 (2010-05-05)

* Depend on javax.servlet instead of org.mortbay.jetty for Servlet API artifact

## 0.2.0 (2010-03-28)

* Distribute Ring as separate Maven artifacts: `ring-core`, `ring-servlet`, `ring-devel`, `ring-jetty-adapter`, and `ring-http-core-adapter`
* The `ring` artifact now just depends on all of these granular artifacts
* Build with Leiningen
* Test with `clojure.test`
* Depend only on stable point-released libraries
* Introduce new middlewares for params, cookies, sessions
* Intro new utils for encoding/decoding, forming responses, and unit testing
* No longer require namespacing of request and response keys
* More documentation, including autodocs
* Various bugfixes

## 0.1.0 (2009-09-06)

* First numbered Ring release
* Adopt ring.{handler,middleware,adapter,util}.* namespace framework
