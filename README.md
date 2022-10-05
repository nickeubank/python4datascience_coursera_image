# VS Code Settings File Pulled by Coursera Docker Build Script

VS Code settings file inherited by our Coursera docker image.

To modify any default vscode settings, simply modify that file, rebuild your image (paying attention to the warning below), and publish.

**Warning**: because docker gets this settings file by pulled in with a `wget` call that does **not** change even if the file changes, docker caching will not update your image if you just click rebuild (it'll assumed it's cached version is fine). To disrupt this caching behavior, add a vacuous (but novel) command of the form `RUN echo "something weird here"` above the last block in our docker commands. That new command will cause docker to assume everything from that point down has to be re-built.
