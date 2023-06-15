# Basic Python 3 TorchServe Platform.sh

This is more hacky than I would have liked as TorchServe is very finicky about its versions. It didn't seem to work with Java 18. And didn't seem to like Python 3.10

So we are using Java 11 and installing Python from LinuxBrew.

Probably still somewhat brittle.

# TODO

Now the most interesting bit is to see if we can get multiple workers on multiple machines to connect to the same torchserve and do some work? 

<p align="center">
<a href="https://console.platform.sh/projects/create-project?template=https://raw.githubusercontent.com/platformsh/template-builder/master/templates/python3/.platform.template.yaml&utm_content=python3&utm_source=github&utm_medium=button&utm_campaign=deploy_on_platform">
    <img src="https://platform.sh/images/deploy/lg-blue.svg" alt="Deploy on Platform.sh" width="180px" />
</a>
</p>

The torchserve was added to the repo thusly:

git subtree add --prefix serve git@github.com:pytorch/serve.git v0.8.1 --squash

## Features

* Java 11
* Python 3.8
* Automatic TLS certificates

## Customizations

The following files are of particular importance.  If using this project as a reference for your own existing project, replicate the changes below to your project.

* The `.platform.app.yaml`, `.platform/services.yaml`, and `.platform/routes.yaml` files have been added.  These provide Platform.sh-specific configuration and are present in all projects on Platform.sh.  You may customize them as you see fit.

## References

* [Python](https://www.python.org/)
* [Python on Platform.sh](https://docs.platform.sh/languages/python.html)
