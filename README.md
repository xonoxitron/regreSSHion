# regreSSHion Exploit (PoC)

## Description
This repository contains an exploit targeting CVE-2024-6387 (regreSSHion), a vulnerability in OpenSSH's server (sshd) on glibc-based Linux systems. It exploits a race condition in the signal handler of OpenSSH, potentially leading to remote code execution as root.

![CVE-2024-6387 PoC](https://github.com/xonoxitron/regreSSHion/blob/main/PoC.png?raw=true)


## Requirements
- Linux system with glibc-based OpenSSH server (tested on Ubuntu, Debian).
- `gcc` compiler installed.
- Basic understanding of compiling and running C programs.
- Permission to test or use such exploits on authorized systems only.

## Usage
1. **Compile the Exploit:**
   ```bash
   gcc -o regreSSHion exploit.c -lpthread
   ```

2. **Run the Exploit:**
   ```bash
   ./regreSSHion <target_ip> <target_port>
   ```

   Replace `<target_ip>` and `<target_port>` with the IP address and port of the vulnerable OpenSSH server.

3. **Interpret Output:**
   - Monitor the terminal for exploitation attempts and feedback.
   - Adjust timing parameters or shellcode as necessary for successful exploitation.

## Shellcode Customization
You can customize the shellcode in the *exploit.c* file to execute different payloads or commands on the target system. The provided shellcode is a basic example that spawns a `/bin/sh` shell. Modify the `shellcode[]` array to suit your specific requirements.

## Legal Disclaimer
**Use of this exploit is at your own risk. By using this software, you agree that:**
- You have permission to test the exploit on systems that you own or have explicit authorization to test.
- You will not use this software for any illegal activities.
- The authors are not responsible for any misuse of this software or any damage caused by it.
- This software is provided "as is" without warranties or conditions of any kind.

**Note:** Unauthorized use or distribution of this exploit may violate local, state, or federal laws. Understand and comply with your local laws and regulations before using or distributing this software.