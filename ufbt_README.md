## ufbt

### What is ufbt ?

ufbt is a tool as same as normal ./fbt software. 

It is designed to be used to develop and debug the fAPs without downloading any firmware code during the development process.

### How to use ufbt ?

ufbt is a tool as same as normal ./fbt software.

There are some useful command you need

`ufbt -h` : show the help information 
> but this command is limited. not all subcommand is documented there

`ufbt update --help`: this command help you manage the firmware SDK and its version/channel. 
> you can switch others firmware SDK by this command like
>
> `ufbt update --index-url=https://up.unleashedflip.com/directory.json`
> 
> will update your SDK to latest unleashedflip SDK

`ufbt status --help`: this command will output the condition of current ufbt settings
> you can see what index you use, what SDK is enabled and version.
> 


`ufbt build`: this command help you build the firmware code.
> you can build the fAP code by this command and same as `ubft`

`ufbt launch`: this command help you launch the app on your device.
> if you not build that fAP code, it will build it automatically and upload it to your device.

`ufbt -c`: clean your build cache and build output.

`ufbt cli`: this command help you launch the console for Cli Application on your device.
> It will conflict with your qFlipper App and you can't use it at the same time.

`ufbt vscode_dist`: will create vscode project folder at current directory.
> you can create app with new folder with `ufbt vscode_dist create APPID=myapp`

```source `ufbt -s env` ```: init toolchain environment for your shell.
> you can use this command to init your shell environment for toolchain. 
