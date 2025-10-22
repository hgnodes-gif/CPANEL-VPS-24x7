# CPANEL VPS 24x7

File Name ``` spam.py ```

24x7 Code ``` 
import time

while True:
    print("HemantGamerzYT")
    time.sleep(1) 
    ```

 ``` python3 spam.py ```

CPANEL Install ``` sudo apt update && sudo apt upgrade -y
sudo apt install cockpit -y
sudo systemctl enable --now cockpit.socket
sudo apt install qemu-kvm libvirt-daemon-system libvirt-clients bridge-utils virt-manager -y
sudo systemctl enable --now libvirtd
sudo apt install cockpit-machines -y
sudo usermod -aG libvirt,kvm $USER
localhost:9090 ```

VM File Name ``` dev.nix ```

``` { pkgs, ... }: {
  # Which nixpkgs channel to use.
  channel = "stable-24.05"; # or "unstable"
  
  # Use https://search.nixos.org/packages to find packages
  packages = [
    pkgs.unzip
    pkgs.openssh
    pkgs.git
    pkgs.qemu_kvm
    pkgs.sudo
    pkgs.cdrkit
    pkgs.cloud-utils
    pkgs.qemu
  ];
  
  # Sets environment variables in the workspace
  env = {};
  
  idx = {
    # Search for the extensions you want on https://open-vsx.org/ and use "publisher.id"
    extensions = [
      "Dart-Code.flutter"
      "Dart-Code.dart-code"
    ];

    workspace = {
      # Runs when a workspace is first created with this `dev.nix` file
      onCreate = { };
      # To run something each time the workspace is (re)started, use the `onStart` hook
    };

    # Disable previews completely
    previews = {
      enable = false;
    };
  };
} 
```

``` bash <(curl -fsSL https://raw.githubusercontent.com/hopingboyz/vms/main/vm.sh) ```

```  ```


