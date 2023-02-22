# AssemblyWorkspace-x86_64-arm-none-eabi
Useful set of tools to get started with the GNU arm-none-eabi toolchain to build assembly projects

## Attributions
* Workspace folder - Dr. Daniel W. Lewis, Santa Clara University

## Install Steps
1) Clone this repository `git clone https://github.com/QuinnMatthews/AssemblyWorkspace-x86_64-arm-none-eabi.git`
2) Move into the new directory `cd AssemblyWorkspace-x86_64-arm-none-eabi`
3) Run the init.sh script `.\init.sh`
   - If you get a permission error `bash: ./init.sh: Permission denied`, you might need to run the following command first: `chmod u+x ./init.sh`
4) Wait for the file to finish downloading then you can move into the workspace folder `cd workspace`

## Using these tools
1) Now that everything is installed you can use the workspace folder you can add your program files to the `src` directory
2) When you are ready to build your files simply run the `make` command
   * `make` is already installed on SMU's genuse servers, additional steps may be required on other platforms

## Remote Tips/Tricks
If you are following this guide to install this on SMU's genuse servers (or any other remote machine) these tips might be helpful
* I recommend using VS Code's `remote - ssh` extension. See: https://code.visualstudio.com/docs/remote/ssh
* To copy files from the remote host back to your local machine, you can use scp. `scp username@remoteHost:/remote/dir/file.txt /local/dir/` 
    * ie: `scp quinnmatthews@genuse60.smu.edu:/users7/cse/qmatthews/source/AssemblyWorkspace-x86_64-arm-none-eabi/workspace/output.bin E:/`
    * To find the full path to a file, in vs code, you can right click on a file and click `Copy Path`
* I recommend generating and using an SSH key for authentication to the remote host, this will allow you to avoid typing in your password several times. This will vary by machine but some general instructions below
  1) **On your local machine** generate a new ssh-key `ssh-keygen -t ed25519 -C "your_email@example.com"` (Exact/Additional Steps may vary)
  2) Upload your new key to github (https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)
  3) **On the remote machine** run import your ssh key `ssh-import-id-gh <github username>`
  
  
