# Go HTTP Function

Welcome to your new Go Function! The boilerplate function code can be found in
[`handle.go`](handle.go). This Function responds to HTTP requests.

## Deploying

```shell
eval $(minikube -p boson-quickstarts docker-env)
func deploy --verbose
```

Describe the deployed function:

```shell
# get the route of the function
func describe helloworld-go
```

Once the function is deployed test the function by invoking it:

```shell
curl (kn service describe helloworld--go -o url)
```

## Development

Develop new features by adding a test to [`handle_test.go`](handle_test.go) for
each feature, and confirm it works with `go test`.

Update the running analog of the funciton using the `func deploy --verbose`, and invoke again to verify the update:

```shell
curl (kn service describe helloworld--go -o url)
```

## Cleanup

Delete the function by running the command `func delete helloworld-go`.

For more, see [the complete documentation]('https://github.com/boson-project/faas/tree/main/docs')
