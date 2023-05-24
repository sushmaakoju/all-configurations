## Configuration

### Scala on MacOS
`brew install coursier/formulas/coursier && cs setup`

#### Install Java on MacOS
`brew install openjdk`

#### Install SBT
`brew install sbt`

### Scala on Windows & Linux

#### Windows Linux Subsystem

##### Enable WSL

- Open Powershell in Administrator mode and 
`dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart` 

##### Enable Virtual

- For Windows 10 (2004), open Powershell in Administrator mode: `dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart` 

- For Windows 10 (1903, 1909), open Powershell in Administrator mode: `Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform -NoRestart`

##### Set WSL 2 as default

- Open Powershell in Administrator mode and 
`wsl --set-default-version 2`

##### Install Linux distribution: Ubunti 20.x or 22.x

- Follow instructions from <a href="https://learn.microsoft.com/en-us/windows/wsl/install-manual">Install Linux distribution</a>

#### Install Scala and Sbt on WSL

- `curl -fL https://github.com/coursier/coursier/releases/latest/download/cs-x86_64-pc-linux.gz | gzip -d > cs && chmod +x cs && ./cs setup`

#### Install Java 20x+ and JDK.
- `sudo apt update `
- `java --version`
- `sudo apt-get install openjdk-20-jdk`
- `java --version`
- `readlink -f $(which java)`
- `vi ~/.bashrc`
- `export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64`
- `source ~/.bashrc`
- `echo $JAVA_HOME`

#### Install SBT
`brew install sbt`

#### Scala extensions on VSCode
- Open VSCode -> Extensions -> Search and Install following:
    - Scala (Metals)
    - Sbt

#### Settings on VSCode
<a href="https://github.com/sushmaakoju/scala-sbt/blob/main/vscode-config.md"> VSCode User & Default settings </a>

#### Install SBT
`$ curl -fL "https://github.com/coursier/launchers/raw/master/cs-x86_64-pc-linux.gz" | gzip -d > cs`
`chmod +x cs`
`./cs setup`
`sbt --version `

