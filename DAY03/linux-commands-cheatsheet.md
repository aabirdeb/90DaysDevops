# Linux Commands Cheat Sheet

## 📁 File & Directory Management

| Command                     | Usage                                                     |
| --------------------------- | --------------------------------------------------------- |
| `pwd`                       | Show the current working directory.                       |
| `ls -la`                    | List all files and directories with detailed information. |
| `cd /path`                  | Change to a specific directory.                           |
| `mkdir <dir>`               | Create a new directory.                                   |
| `touch <file>`              | Create an empty file.                                     |
| `cp <source> <dest>`        | Copy a file or directory.                                 |
| `mv <source> <dest>`        | Move or rename a file or directory.                       |
| `rm <file>`                 | Delete a file.                                            |
| `rm -rf <dir>`              | Recursively delete a directory and its contents.          |
| `find /path -name "<name>"` | Search for files or directories by name.                  |

## 📄 File Viewing & Text Processing

| Command                | Usage                                           |
| ---------------------- | ----------------------------------------------- |
| `cat <file>`           | Display the contents of a file.                 |
| `less <file>`          | View a file one page at a time.                 |
| `head -n 10 <file>`    | Display the first 10 lines of a file.           |
| `tail -n 10 <file>`    | Display the last 10 lines of a file.            |
| `tail -f <file>`       | Continuously monitor new lines added to a file. |
| `grep "<text>" <file>` | Search for matching text inside a file.         |
| `wc -l <file>`         | Count the number of lines in a file.            |

## ⚙️ System & Process Management

| Command        | Usage                                                   |
| -------------- | ------------------------------------------------------- |
| `ps aux`       | Display currently running processes.                    |
| `top`          | Monitor processes and system resource usage.            |
| `kill <PID>`   | Terminate a process using its process ID.               |
| `df -h`        | Display filesystem disk usage in human-readable format. |
| `du -sh <dir>` | Display the total disk usage of a directory.            |
| `free -h`      | Display available and used system memory.               |
| `uptime`       | Show system uptime and load averages.                   |
| `uname -a`     | Display kernel and system information.                  |

## 🔐 Users & Permissions

| Command                   | Usage                                             |
| ------------------------- | ------------------------------------------------- |
| `whoami`                  | Show the currently logged-in user.                |
| `id`                      | Display user ID, group ID, and group memberships. |
| `chmod 755 <file>`        | Change file or directory permissions.             |
| `chown user:group <file>` | Change file ownership and group.                  |
| `sudo <command>`          | Run a command with elevated privileges.           |

## 🌐 Networking

| Command        | Usage                                                      |
| -------------- | ---------------------------------------------------------- |
| `ping <host>`  | Test network connectivity to a host.                       |
| `ip addr`      | Display network interfaces and IP addresses.               |
| `dig <domain>` | Query DNS records for a domain.                            |
| `curl <URL>`   | Send HTTP/HTTPS requests and test API or web connectivity. |
| `ss -tulnp`    | Show listening TCP/UDP ports and associated processes.     |
| `ip route`     | Display the system routing table.                          |

## 📦 Package Management

### Ubuntu / Debian

| Command                      | Usage                                       |
| ---------------------------- | ------------------------------------------- |
| `apt list --installed`       | List installed packages.                    |
| `sudo apt update`            | Refresh the package repository information. |
| `sudo apt install <package>` | Install a package.                          |
| `sudo apt remove <package>`  | Remove an installed package.                |

### RHEL / CentOS / Rocky Linux

| Command                      | Usage                                                |
| ---------------------------- | ---------------------------------------------------- |
| `rpm -qa`                    | List all installed RPM packages.                     |
| `dnf list installed`         | List installed packages on newer RHEL-based systems. |
| `sudo dnf install <package>` | Install a package.                                   |
| `sudo dnf remove <package>`  | Remove a package.                                    |

## 🛠️ Services & Logs

| Command                               | Usage                                     |
| ------------------------------------- | ----------------------------------------- |
| `systemctl status <service>`          | Check the status of a systemd service.    |
| `sudo systemctl start <service>`      | Start a service.                          |
| `sudo systemctl stop <service>`       | Stop a service.                           |
| `sudo systemctl restart <service>`    | Restart a service.                        |
| `systemctl list-units --type=service` | List systemd services.                    |
| `journalctl -u <service>`             | View logs for a specific systemd service. |
| `journalctl -u <service> -f`          | Follow service logs in real time.         |

## 🗜️ Archive & Compression

| Command                          | Usage                                 |
| -------------------------------- | ------------------------------------- |
| `tar -czvf archive.tar.gz <dir>` | Create a compressed tar archive.      |
| `tar -xzvf archive.tar.gz`       | Extract a `.tar.gz` archive.          |
| `zip -r archive.zip <dir>`       | Compress a directory into a ZIP file. |
| `unzip archive.zip`              | Extract a ZIP archive.                |

## 💡 Quick Troubleshooting

```bash
df -h                  # Check disk space
free -h                # Check memory
top                    # Check CPU/process usage
systemctl status nginx # Check service status
journalctl -u nginx    # Check service logs
ss -tulnp              # Check listening ports
ping 8.8.8.8           # Test network connectivity
dig google.com         # Test DNS resolution
curl -I https://google.com  # Test HTTP/HTTPS connectivity
```

> **Warning:** Commands such as `rm -rf`, `chmod`, `chown`, and commands executed with `sudo` can make significant system changes. Verify the target before running them.
