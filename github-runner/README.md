https://github.com/asasar/ibm-context-forge/settings/actions/runners/new?arch=x64&os=linux


Download
# Create a folder
$ mkdir actions-runner && cd actions-runnerCopied!# Download the latest runner package
$ curl -o actions-runner-linux-x64-2.331.0.tar.gz -L https://github.com/actions/runner/releases/download/v2.331.0/actions-runner-linux-x64-2.331.0.tar.gz# Optional: Validate the hash
$ echo "5fcc01bd546ba5c3f1291c2803658ebd3cedb3836489eda3be357d41bfcf28a7  actions-runner-linux-x64-2.331.0.tar.gz" | shasum -a 256 -c# Extract the installer
$ tar xzf ./actions-runner-linux-x64-2.331.0.tar.gz
Configure

# Create the runner and start the configuration experience

$ ./config.sh --url https://github.com/asasar/ibm-context-forge --token << Complete>>

# Last step, run it!
$ ./run.sh


# Installing the service
sudo ./svc.sh install

Alternatively, the command takes an optional user argument to install the service as a different user.

./svc.sh install USERNAME

Starting the service
Start the service with the following command:

sudo ./svc.sh start

Using your self-hosted runner
# Use this YAML in your workflow file for each job
runs-on: self-hosted
