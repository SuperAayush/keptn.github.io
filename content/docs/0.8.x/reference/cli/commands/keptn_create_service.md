---
date: "2020-12-23T13:20:36+01:00"
title: "keptn create service"
slug: keptn_create_service
---
## keptn create service

Creates a new service

### Synopsis

Creates a new service with the provided name in the specified project.

**Note:** This command is different from keptn onboard service which requires a Helm chart.


```
keptn create service SERVICENAME --project=PROJECTNAME [flags]
```

### Examples

```
keptn create service carts --project=sockshop
```

### Options

```
  -h, --help             help for service
  -p, --project string   The project in which to create the service
```

### Options inherited from parent commands

```
      --mock               Disables communication to a Keptn endpoint
  -n, --namespace string   Specify the namespace where Keptn should be installed, used and uninstalled in (default keptn). (default "keptn")
  -q, --quiet              Suppresses debug and info messages
  -v, --verbose            Enables verbose logging to print debug messages
```

### SEE ALSO

* [keptn create](../keptn_create/)	 - Creates a new project or service

###### Auto generated by spf13/cobra on 23-Dec-2020