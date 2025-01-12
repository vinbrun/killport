# **killport**

A simple Bash script to kill processes by port number with a single command.

## **Features**
- Find and kill processes running on a specific port with a single command.
- Defaults to killing processes on port `3000` if no port is provided.
- Lightweight and easy to use.

---

## **Installation**

1. **Download the Script**
   ```bash
   wget https://raw.githubusercontent.com/vinybk/killport/main/killport
   ```

2. **Make it Executable**
   ```bash
   chmod +x killport
   ```

3. **(Optional) Add to PATH for Easy Access**
   Move the script to a directory in your system's PATH:
   ```bash
   sudo mv killport /usr/local/bin/
   ```
   This allows you to run `killport` from anywhere.

---

## **Usage**

### **Basic Command**
To kill a process running on port `3000`:
```bash
killport
```

### **Specify a Port**
To kill a process on a different port:
```bash
killport <port_number>
```
Example:
```bash
killport 8080
```

### **Output**
- If a process is found and killed:  
   ```bash
   Killed process [process_name] running on port [port_number]
   ```
- If no process is found on the port:  
   ```bash
   No process found running on port [port_number]
   ```

---

## **Requirements**
- **Linux** with Bash installed.
- `lsof` command available (most Linux distributions include it by default).

---

## **Tips**
- If you frequently kill processes on a specific port, consider aliasing the script in your `.bashrc` or `.zshrc`:
   ```bash
   alias killnode='killport 3000'
   ```
   Run `source ~/.bashrc` or `source ~/.zshrc` to apply changes.

---

## **Contributing**
Contributions are welcome! If you'd like to add features or improve the script:
1. Fork the repository.
2. Make your changes.
3. Submit a pull request.

---

## **License**
This project is licensed under the MIT License.
