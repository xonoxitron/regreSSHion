# regreSSHion Exploit

## Description
This repository contains an exploit targeting CVE-2024-6387 (regreSSHion), a vulnerability in OpenSSH's server (sshd) on glibc-based Linux systems. It exploits a race condition in the signal handler of OpenSSH, potentially leading to remote code execution as root.

## Requirements
- Linux system with glibc-based OpenSSH server (tested on Ubuntu, Debian).
- `gcc` compiler installed.
- Basic understanding of compiling and running C programs.
- Permission to test or use such exploits on authorized systems only.

## Usage
1. **Compile the Exploit:**
   ```bash
   gcc -o exploit 7etsuo-regreSSHion.c -lpthread
   ```

2. **Run the Exploit:**
   ```bash
   ./exploit <target_ip> <target_port>
   ```

   Replace `<target_ip>` and `<target_port>` with the IP address and port of the vulnerable OpenSSH server.

3. **Interpret Output:**
   - Monitor the terminal for exploitation attempts and feedback.
   - Adjust timing parameters or shellcode as necessary for successful exploitation.

## Shellcode Customization
You can customize the shellcode in the *exploit.c* file to execute different payloads or commands on the target system. The provided shellcode is a basic example that spawns a `/bin/sh shell`. Modify the `shellcode[]` array to suit your specific requirements.

## Legal Disclaimer
Use this exploit responsibly and only on systems where you have explicit permission to test. Unauthorized use or distribution may violate local, state, or federal laws. The authors are not responsible for any misuse of this exploit.

---

This `README.md` provides a basic outline of what the repository contains, the requirements to use it, how to compile and run the exploit, and a legal disclaimer about responsible use. Adjust the content based on your specific exploit's details and any additional instructions or considerations you want to provide to users.
