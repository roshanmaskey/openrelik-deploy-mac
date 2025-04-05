# Develop/Deploy OpenRelik on macOS

If you want to use `podman` instead of `docker` on Apple Silicon macOS to develop, or deploy OpenRelik, this is the guide that will help you.

The repo provides the updated `install.sh` script to work with `podman`.

## Installation

1. Install Homebrew (https://brew.sh)
   ```shell
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```
2. Install `podman`

   ```shell
   brew install podman
   brew install podman-compose
   ```
   
3. Download the install script
   
   ```shell
   curl -s -O https://raw.githubusercontent.com/roshanmaskey/openrelik-deploy-mac/refs/heads/main/podman/install.sh
   ```

4. Install OpenRelik

  ```shell
  bash install.sh
  ```

5. Stat/Stop OpenRelik
   
  Run the following commands to stop OpenRelik containers.

  ```shell
  cd openrelik
  podman-compose down
  ```

  Run the following commands to start OpenRelik containers.

  ```shell
  cd openrelik
  podman-compose up -d
  ``` 
