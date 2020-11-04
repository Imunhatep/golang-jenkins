golang-jenkins
-----------

### About
This is a API client of Jenkins API written in Go. Forked cause original library gone stale, this one include all Mrs from original, plus supporting jenkins sub-folder projects.

### Usage
`import "github.com/imunhatep/golang-jenkins"`

Configure authentication and create an instance of the client:

```go
auth := &gojenkins.Auth{
  Username: "[jenkins user name]",
  ApiToken: "[jenkins API token]",
}
jenkins := gojenkins.NewJenkins(auth, "[jenkins instance base url]")
```

Make calls against the desired resources:
```go
job, err := jenkins.GetJob("[job name]")
```

#### License
golang-jenkins is licensed under the MIT LICENSE. See [./LICENSE](./LICENSE)
