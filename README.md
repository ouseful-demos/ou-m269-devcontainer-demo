# ou-m269-devcontainer-demo

Unofficial minimal dev container demo for M269.

Access the Python environment provided by the online VCE Dokcer container within a browser based VS Code IDE using GitHub Codespaces and simple `.devcontainer` script.

![Launch codespace](images/codespace_launch.png)

Wait for the container to be built:

![Wait for container to build](images/container_build.png)

I have my GitHub Codespace environment configured to attempt to launch into JupyterLab and need to manually open the container into a VS Code environment. *Using GitHub default settings, the container would ordinarily open into a VS Code environment automatically.*

![Open container in VS Code](images/open_in_vs_code.png)

Any notebooks uploaded to the environment can be viewed and executed in VS Code. However, it is also possible to run the classic notebook environment from Codespaces too.

## Using the VS Code Environment

The VS Code environment is preinstalled with a Git extension.

If you launch the devcontainer powered Codespace from your own repository you can commit updates back to the repository you started the container from. Updates will also persist inside the container.

## Initialising the environment and Using the Classic Notebook Environment

To initialise the environment and to access the classic notebook environment, in the VS Code terminal run the command:

`start.sh`

This will run any required initialisation routines in the container and start the classic notebook server.

The notebook server port will be forwarded automatically:

![Automatically forwarded port](images/forwarded_port.png)

Use the password `M269 23J` to access the classic notebook server UI:

![enter Jupyter server password "M269 23J"](images/server_pwd.png)

You can check the password by running the command `jupyter server list` in a new terminal:

![View list of jupyter servers by running `jupyter server list`](images/list_servers.png)

