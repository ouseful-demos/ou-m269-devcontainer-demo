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


## Using the Classic Notebook Environment

To access the classic notebook environment, in the VS Code terminal run the command:

`jupyter nbclassic`


![Issue 'jupyter nbclassic' command in termnial](images/jupyter_nbclassic_run.png)

This will start the classic notebook server, although when I ran it, it upset the VS Code browser, which prompted from a reload.

![Reload prompt](images/reload_prompt.png)

Clicking the reload button and everything seems to be running okay:

![Jupyter server running log](images/server_running.png)

We now need to expose the server port. In VS Code, select the *Ports* tab and create a new port, setting it to `8888`:

![Add a new exposed port (8888)](images/create_port.png)

If you hover the mouse over this port entry you can raise a menu that will open that location in your browser:

![Open link in browser pop-up](images/open_in_browser.png)

Use the password `M269 23J` to access the classic notebook server UI:

![enter Jupyter server password "M269 23J"](images/server_pwd.png)

You can check the password by running the command `jupyter server list` in a new terminal:

![View list of jupyter servers by running `jupyter server list`](images/list_servers.png)

