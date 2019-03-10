# Heartbeat input plugin for [Fluentd](http://github.com/fluent/fluentd)

## Overview

This is a fluentd input plugin to generate events periodically as a means to generate heartbeat with any custom message. By designing the heartbeat plugin as an input plugin, it can be chained with any fluentd output plugin to deliver heartbeats using any protocol. 