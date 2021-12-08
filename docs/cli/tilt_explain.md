---
title: Tilt CLI Reference
layout: docs
sidebar: reference
hideEditButton: true
---
## tilt explain

Get documentation for a resource

### Synopsis

List the fields for supported resources. This command describes the fields associated with each supported API resource. Fields are identified via a simple JSONPath identifier:<type> .<fieldName> [.<fieldName> ] Add the --recursive flag to display all of the fields at once without descriptions. Information about each field is retrieved from the server in OpenAPI format.

```
tilt explain RESOURCE
```

### Examples

```
  # Get the documentation of the resource and its fields
  tilt explain cmds
  # Get the documentation of a specific field of a resource
  tilt explain cmds.spec.args
```

### Options

```
      --api-version string   Get different explanations for particular API version (API group/version)
  -h, --help                 help for explain
      --host string          Host for the Tilt HTTP server. Only necessary if you started Tilt with --host. Overrides TILT_HOST env variable. (default "localhost")
      --port int             Port for the Tilt HTTP server. Only necessary if you started Tilt with --port. Overrides TILT_PORT env variable. (default 10350)
      --recursive            Print the fields of fields (Currently only 1 level deep)
```

### Options inherited from parent commands

```
  -d, --debug                          Enable debug logging
      --klog int                       Enable Kubernetes API logging. Uses klog v-levels (0-4 are debug logs, 5-9 are tracing logs)
      --log-flush-frequency duration   Maximum number of seconds between log flushes (default 5s)
  -v, --verbose                        Enable verbose logging
```

### SEE ALSO

* [tilt](tilt.html)	 - Multi-service development with no stress

###### Auto generated by spf13/cobra on 3-Dec-2021