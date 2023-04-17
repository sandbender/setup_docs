
# How to use mybinder.org to setup a NodeJS-enabled temporary Jupyter server

1. Visit [mybinder.org](https://mybinder.org/v2/gh/jupyter/docker-stacks/main?urlpath=lab/tree/README.ipynb) to initialize and boot a fresh, temporary Jupyter system.

2. Once started, use the main "File" menu of the Jupyter interface to navigate to the "New" -> "Terminal" menu item and click it to open a Terminal tab in your main Jupyter workspace.

3. Copy and paste the following commands into the now-running Terminal window of your Jupyter workspace:

```
    mkdir ~/bin
    source ~/.profile
    npm config set prefix $HOME
    npm install -g ijavascript
    ln -s ~/bin/ijs /opt/conda/bin/ijs
    ln -s ~/bin/ijsconsole /opt/conda/bin/ijsconsole
    ln -s ~/bin/ijsinstall /opt/conda/bin/ijsinstall
    ln -s ~/bin/ijskernel /opt/conda/bin/ijskernel
    ln -s ~/bin/ijsnotebook /opt/conda/bin/ijsnotebook
    ijsinstall
```

4. Once the above commands complete, use the "New Launcher" option of the main "File" menu of the Jupyter interface to open a new Launcher tab in the workspace.

5. You may need to wait a moment before "JavaScript (Node.js)" appears as an option beside "Python 3 (ipykernel)" under the main "Notebook" section of this screen.

6. Once you see the "JavaScript" icon in the launcher tab, you can click it to replace the launcher tab with a Notebook tab running the Node.js kernel.
