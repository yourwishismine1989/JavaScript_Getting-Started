# JavaScript_Getting-Started
A quick how to with your first application example

## __install JavaScript__
 
### Setup linux distro (tested on Ubuntu 22.04 on 09/26/2023)
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash ### https://github.com/nvm-sh/nvm
    source ~/.bashrc
    nvm install --lts
    npm install --global npm@10.1.0 ### or later if available

 
### Setup Windows (tested on Windows 11 on 09/26/2023)
    C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (right-click -> Run as administrator)
        Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
        exit (or close Administrator: Windows PowerShell window)
    C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        Invoke-RestMethod -Uri get.scoop.sh | Invoke-Expression
        scoop install git
        scoop bucket add extras
        exit (or close Windows PowerShell window)
    C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe (right-click -> Run as administrator)
        scoop install vcredist-aio
        exit (or close Administrator: Windows PowerShell window)
    * C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
        scoop install nodejs-lts
        scoop install mysql-lts ### Run 'mysqld --standalone' or 'mysqld --console' to start the Database
        scoop install mysql-workbench
        scoop install mongodb
        scoop install mongosh
        scoop install mongodb-compass
        code
            Add the following VSCode extensions to VSCode
                ES Lint
                Docker
                GitLens
                isort
                JavaScript and TypeScript Nightly
                learn-markdown
                Live Preview
                MySQL
                PowerShell
                Pylance
                Pylint
                Python
                Reactjs code snippets
                React Native Tools
                ShellCheck
            close VSCode window
 
## __hello-world__ (tested on Ubuntu 22.04 on 09/26/2023)
**__hello-world__** (tested on Ubuntu 22.04 on 09/26/2023)
    mkdir hello-world
    cd ./hello-world/
    npm init --yes
    touch index.js
    nano ./index.js
    const readline = require("readline");
    const rl = readline.createInterface({
        input: process.stdin,
        output: process.stdout
    });
    
    rl.question("What is your name ? ", (name) => {
            console.log(`Hello, ${name}`);
            rl.close();
    });
    CTRL-o -> ENTER
    CTRL-x
    node ./index.js