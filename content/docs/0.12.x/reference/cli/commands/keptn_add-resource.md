---
date: "2022-01-31T09:42:04Z"
title: "keptn add-resource"
slug: keptn_add-resource
---
## keptn add-resource

Adds a local resource to a service within your project in the specified stage

### Synopsis

Adds a local resource to a service within your project in the specified stage. The resource is then stored within the Git repository.

This command allows adding, for example, *test files* to a service, which will then be used by a test service (e.g., jmeter-service) during the continuous delivery.

To specify a unique resource identifier (URI) for this resource, the optional flag *--resourceUri* can be set to a file path. 
By default, the URI is set to the file path specified at the *--resource* flag. 
From a technical perspective, the file provided via the *--resource* flag is stored with the path and name specified within *--resourceUri* flag.

**The target location of the resource:**

- *--project* - is mandatory. The resource will be added to the root folder in the master branch. 
- *--stage* - is optional (when the *--service* flag is not used). The resource will be added to the root folder in the stage branch.
- *--service* - is optional. The resource will be added to the service folder in the stage branch.


```
keptn add-resource --project=PROJECT --stage=STAGE --service=SERVICE --resource=FILEPATH --resourceUri=FILEPATH [flags]
```

### Examples

```
keptn add-resource --project=musicshop --stage=hardening --service=catalogue --resource=slo.yaml
keptn add-resource --project=musicshop --stage=hardening --service=catalogue --resource=slo-quality-gates.yaml --resourceUri=slo.yaml
keptn add-resource --project=sockshop --stage=dev --service=carts --resource=./jmeter.jmx --resourceUri=jmeter/functional.jmx
keptn add-resource --project=rockshop --stage=production --service=shop --resource=./basiccheck.jmx --resourceUri=jmeter/basiccheck.jmx
keptn add-resource --project=keptn --service=keptn-control-plane --all-stages --resource=0.7.3_keptn-installer.tgz --resourceUri=helm/keptn-control-plane.tgz
```

### Options

```
      --all-stages           Add resource to all stages (can not be used together with (--stage)
  -p, --project string       The name of the project
  -r, --resource string      Path pointing to the resource on your local file system
      --resourceUri string   Optional: Location where the resource should be stored within the config repo. If empty, The name of the resource will be the same as on your local file system
      --service string       The name of the service within the project
  -s, --stage string         The name of the stage (cannot be used together with (--all-stages)
```

### Options inherited from parent commands

```
      --config-file string   Specify custom Keptn Config file path (default: ~/.keptn/config)
  -h, --help                 help
      --mock                 Disables communication to a Keptn endpoint
  -n, --namespace string     Specify the namespace where Keptn should be installed, used and uninstalled in (default "keptn")
  -q, --quiet                Suppresses debug and info messages
  -v, --verbose              Enables verbose logging to print debug messages
  -y, --yes                  Assume yes for all user prompts
```

### SEE ALSO

* [keptn](../keptn/)	 - The CLI for using Keptn

###### Auto generated by spf13/cobra on 31-Jan-2022