GoCD Hipchat Notification Plugin [![Build Status](https://travis-ci.org/PagerDuty/gocd-hipchat-plugin.svg?branch=master)](https://travis-ci.org/PagerDuty/gocd-hipchat-plugin)
================================

To install:

* Run `sbt clean assembly`
* Copy `gocd-hipchat-plugin.jar` from `target/scala-2.10/` to the `plugins/external` folder on your GoCD server
* Create a file named ".hipchat" in the home folder for all agents and servers, containing the following:
```
hipchat_server=http://{{your_hipchat_server_here}}
```
* Restart the server
* HipChat notification is now available as a task plugin

Environment variables can be inserted into messages using bash $ notation. If the GO_BASE_URL
environment variable is set, you can use $BUILD_URL to insert a link to the current build
