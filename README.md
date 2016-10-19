### Demo for [Cloud Foundry V3 API](http://v3-apidocs.cloudfoundry.org/)

Use [v3-cli-plugin](https://github.com/cloudfoundry/v3-cli-plugin)

```
cf install-plugin https://github.com/cloudfoundry/v3-cli-plugin/releases/download/0.6.5/v3-cli-plugin.osx
cf v3-push hello -b ruby_buildpack
cf v3-run-task hello say "./hello.rb"
```

You'll see


``` console
$ cf v3-apps
name    total_desired_instances
hello   0

$ cf v3-run-task hello say "./hello.rb"
OK

Running task say on app hello...

Tailing logs for app hello...

2016-10-20T03:39:28.31+0900 [APP/TASK/say/0]OUT Creating container
2016-10-20T03:39:28.99+0900 [APP/TASK/say/0]OUT Successfully created container
2016-10-20T03:39:30.01+0900 [APP/TASK/say/0]OUT Hello World
2016-10-20T03:39:30.01+0900 [APP/TASK/say/0]OUT Exit status 0
2016-10-20T03:39:30.03+0900 [APP/TASK/say/0]OUT Destroying container
Task 803952e1-400c-4230-a62d-8083f317b071 successfully completed.
```
