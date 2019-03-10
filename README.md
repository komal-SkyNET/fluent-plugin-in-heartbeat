# Heartbeat input plugin for [Fluentd](http://github.com/fluent/fluentd)

## Overview

This is a fluentd input plugin to generate events periodically as a means to generate heartbeat with any custom message. By designing the heartbeat plugin as an input plugin, it can be chained with any fluentd output plugin to deliver heartbeats using any protocol. 

##Usage

<source>
    @type heartbeat
    rate 1          #Generate 1 heartbeat per $interval configured
    tag heartbeat.from.fluentd
    interval 5      #Generate heartbeat every 5 seconds
    dummy "{\"message\": \"fluentd-is-alive"}" #custom message to be in heartbeat | default: fluentd-is-alive
</source>

##Note

This plugin is based on fluentd core in_dummy plugin. 