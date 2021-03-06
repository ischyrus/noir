##Changes for 1.2.0

* Refactored for Clojure 1.3.0 support
* Refactored server to enable custom noir handler creation
* Added url decoding for routes. (defpage "/hey how" ...) will work now.
* Added noir.util.gae to get Noir up on Google App Engine
* Added named routes 
* Added noir.request/ring-request
* Added url-for to query named routes
* Added noir.server/load-view-ns
* Added a :resource-root option to the server
* Added a :cookie-attrs option to the server
* Added post-route
* Added signed cookies
* Added compojure-route and custom-handler to handle integration with other libs
* Changed noir.validation/errors? will now return if any errors exist if no fields are supplied.
* Fixed noir.validation/is-email? to use a better regex
* Fixed and improved noir.util.s3
* Fixed incorrect header setting for noir.response/xml
* Fixed custom middleware preserves order
* Fixed bugs in cookie handling that would cause incorrect retrieval
* Fixed some issues with exceptions to make the 500 page more resilient
* Moved to latest compojure/ring/hiccup
* Added tons of tests


##Changes for 1.1.0

* Added session/flash-put! and sesion/flash-get
* Added alternative session storage via the :session-store server option
* Removed dependency on contrib
* Added defaults for session/get and cookies/get
* Added gen-handler for interop with other ring-based libraries
* Added test utilities under noir.util.test
* Added noir.util.middleware
* Moved to latest compojure/ring/hiccup
* Added server/stop server/restart
* Fixed bug where server/start wasn't returning a server object
