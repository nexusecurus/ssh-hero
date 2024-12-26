
# <p align="center">SSH-HERO - SSH Management Terminal GUI Tool </p> 
 <p align="center">powered by NexuSecurus&trade;</p> 


<div style="text-align:center">
    <img src="images/nexusecurus.png" alt="NexuSecurus">
</div>

<p align="center">
  <table>
    <tr>
      <th>Supported HW</th>
      <th>Supported OS</th>
      <th>Code Stats</th>
      <th>Audience</th>
      <th>Type</th>
      <th>License</th>
    </tr>
    <tr>
      <td><img src="https://img.shields.io/badge/Architecture-x86_32/64-blue?logo=intel&logoColor=white"></td>
      <td><img src="https://img.shields.io/badge/-macOS-black?logo=apple"></td>
      <td><img src="https://img.shields.io/badge/Shell-Used-green?logo=bash"></td>
      <td><img src="https://img.shields.io/badge/Terminal-%20Users-%23197aaa?logo=linux&logoColor=white"></td>
      <td><img src="https://img.shields.io/badge/Menu-Based-brightyellow?logo=menu-framework"></td>
      <td><img src="https://img.shields.io/badge/License-MIT-blue.svg"></td>
    </tr>
    <tr>
      <td><img src="https://img.shields.io/badge/ARM-Architecture-blue"></td>
      <td><img src="https://img.shields.io/badge/Linux-orange?logo=linux"></td>
      <td><img src="https://img.shields.io/badge/Markdown-Used-yellow?logo=markdown"></td>
      <td><img src="https://img.shields.io/badge/Linux-macOS-blue"></td>
      <td><img src="https://img.shields.io/badge/Terminal-TUI-blue"></td>
    </tr>
  </table>
</p>


<br>
<br>
<br>


---

# TABLE OF CONTENTS
- [SSH-HERO - SSH Management Terminal GUI Tool ](#ssh-hero---ssh-management-terminal-gui-tool-)
- [TABLE OF CONTENTS](#table-of-contents)
- [SSH-Hero (SSH Key Manager)](#ssh-hero-ssh-key-manager)
  - [Features](#features)
  - [Menu Options](#menu-options)
    - [Create SSH Keys](#create-ssh-keys)
    - [Delete SSH Keys](#delete-ssh-keys)
    - [Load SSH Keys into Agent](#load-ssh-keys-into-agent)
    - [Unload SSH Keys from Agent](#unload-ssh-keys-from-agent)
    - [Remove IP from Known Hosts](#remove-ip-from-known-hosts)
    - [Kill Agent Processes](#kill-agent-processes)
  - [Repository](#repository)
  - [Version](#version)
  - [Hardware Requirements](#hardware-requirements)
  - [Software Dependencies on Linux/macOS (Auto Install on First Run)](#software-dependencies-on-linuxmacos-auto-install-on-first-run)
  - [Installation Instructions](#installation-instructions)
    - [1. Clone the Repository](#1-clone-the-repository)
    - [2. Change into the Cloned Directory](#2-change-into-the-cloned-directory)
    - [3. Give execution permission to file](#3-give-execution-permission-to-file)
    - [4. Add program to be available System-Wide **privilege escalation required** (OPTIONAL)](#4-add-program-to-be-available-system-wide-privilege-escalation-required-optional)
    - [5. Verify Installation](#5-verify-installation)
    - [6. Usage without adding to System-Wide PATH (Must be run inside cloned directory ssh-hero)](#6-usage-without-adding-to-system-wide-path-must-be-run-inside-cloned-directory-ssh-hero)
    - [7. Usage with System-Wide PATH](#7-usage-with-system-wide-path)
  - [Special Notes on Security](#special-notes-on-security)
  - [Contributing](#contributing)
  - [License](#license)
  - [Disclaimer](#disclaimer)
  - [Author](#author)
    - [Contact Information](#contact-information)

---
---

# SSH-Hero (SSH Key Manager)

**SSH-Hero** is a versatile SSH key management tool designed for secure and efficient handling of SSH key operations. It uses a retro GUI which is user-friendly, making it accessible to users of all skill levels.  It supports x86 (32/64-bit) and ARM architectures, including Apple Silicon, and provides essential features for developers, system administrators, and DevOps engineers, or simple day to day users.

Was developed using shell scripting with a focus on simplicity and minimum dependencies requirements.

If you have a bash shell environment, you can use SSH-Hero with minimal setup or no setup at all based on your os.

---
---

## Features
- **Manage SSH keys**: Load, Remove, list, and unload keys securely.
- **Cross-platform compatibility**: Works on x86 and ARM architectures.
- **Lightweight and simple**: Minimal dependencies with powerful functionality.

---
---

## Menu Options


### Create SSH Keys
1. Select **"Create SSH Keys"** from the menu.
2. Follow the prompts to specify key details such as location, filename, type, bits, and comment.

### Delete SSH Keys
1. From the main menu, select **"Delete SSH Keys"**.
2. Choose an existing key to delete.

### Load SSH Keys into Agent
1. Select **"Load SSH Keys"** from the menu.
2. Choose a private key to load into the SSH agent.

### Unload SSH Keys from Agent
1. Select **"Unload SSH Keys"** to remove loaded key into the agent.

### Remove IP from Known Hosts
1. Select **"Remove IP"**.
2. Enter the IP address and port (default is 22) to remove entries from your `known_hosts` file.

### Kill Agent Processes
1. Use this option when you are done using the program.
2. It will terminate all SSH agent processes, ensuring that no keys remain loaded.



## Repository
Find the source code on GitHub:  
[https://www.github.com/nexusecurus/ssh-hero.git](https://www.github.com/nexusecurus/ssh-hero.git)

---
---

## Version
**Current Version**: 0.1b (Beta)

---
---

## Hardware Requirements
- **Supported Architectures**:
  - x86 (32-bit and 64-bit)
  - ARM (e.g., Raspberry Pi, Apple Silicon)
- **Recommended System Specifications**:
  - Minimum: If you can install linux on your device, it works.
  - Recommended: 128MB RAM, 486 120MHz processor or Higher

---
---

## Software Dependencies on Linux/macOS (Auto Install on First Run)
Ensure the following are installed on your system before using SSH-Hero:

- **macOS**: Brew (macOS package manager) - Must be mannually installed if not already present.

- **Linux/macOS**: dialog, openssh-client or openssh-server - These will be automatically installed if not present during the first run of SSH-Hero.

---
---

## Installation Instructions

### 1. Clone the Repository
```bash
git clone https://www.github.com/nexusecurus/ssh-hero.git
```
### 2. Change into the Cloned Directory
```bash
cd ssh-hero
```

### 3. Give execution permission to file

```bash
chmod +x ssh-hero
```

### 4. Add program to be available System-Wide **privilege escalation required** (OPTIONAL)
```bash
sudo cp ssh-hero /usr/local/bin/
```

### 5. Verify Installation
```bash
ssh-hero -v
```
This should display the version of SSH-Hero installed on your system.

### 6. Usage without adding to System-Wide PATH (Must be run inside cloned directory ssh-hero)
```bash
./ssh-hero                  --> Run SSH-Hero interactively.
./ssh-hero -h or --help     --> Display help message.
./ssh-hero -v or --version  --> Display version information.
```

### 7. Usage with System-Wide PATH
```bash
ssh-hero                    --> Run SSH-Hero interactively.
ssh-hero -h or --help       --> Display help message.
ssh-hero -v or --version    --> Display version information.
```

---
---

## Special Notes on Security

We all know that use ssh-agent inside a program is a pain the butt, cause it opens up a new PID every time you run it, and you end up with a bunch of agents running around.

Due to macOS ssh nature, the problem was solved, but when it comes to Linux, i wasn't able to found a proper solution without compromising on security.

So, just for security advice, make sure of the following:

- When you don't need the loaded keys anymore, **unload** and **KILL** all keys and SSH agents to ensure that loaded keys are no longer available in the system after the session ends.
- There's both a **Unload Keys** and **Kill All Agents** option in the menu.

---
---

## Contributing

Feel free to fork the repository, submit pull requests, or report issues on GitHub:
https://www.github.com/nexusecurus/ssh-hero.git

---
---

## License

SSH-Hero is released under the MIT License.

---
---


## Disclaimer

SSH-Hero uses the ssh original built-in commands to the generate, load and unload key functions. This software is basically an automation and GUI version for those wanting a prettier version, or if you are a newcomer to linux and want a easier/simpler way of managing SSH Keys. Although SSH-Hero is in beta (v0.1), every effort was made to ensure reliability, users shouldn't be worried of any type of security issues.

---
---

Nevertheless,
The authors of SSH-Hero are not responsible for any misuse or security breaches caused by the use of this software. Use it at your own risk.

## Author
**Company**: NexusSecurus  
**Website**: https://www.nexusecurus.com/   
**Email**: github@nexusecurus.com   
**GitHub**: [github.com/nexusecurus]    
**Developer**: prenats  
**Developer GitHub**: [github.com/prenats]

### Contact Information

For support, feedback, or inquiries, please contact:
- **Email**: support@nexusecurus.com

---
---
