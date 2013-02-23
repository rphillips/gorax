# gorax

**This library is still in the very early stages of development. Unless you want to contribute, it probably isn't what you want**

## Cloud Monitoring Example

```go
package main

import (
  "rackspace/monitoring"
  "rackspace/identity"
  "encoding/json"
  "fmt"
)

func main() {
  cm := monitoring.MakePasswordMonitoringClient("https://monitoring.api.rackspacecloud.com/v1.0", identity.USIdentityService, "username", "password")
  cm.SetDebug(true)
  checks, err := cm.ListChecks("enuzk2tiph")
  fmt.Printf("%s\n", checks)
  fmt.Printf("%s\n", err)
}
```
