# shell-tools-lite

A lightweight collection of handy shell utilities for Linux productivity, including GPU monitoring, process management, and background job control.

## 🧰 Included Commands

| Command   | Description                                      |
|-----------|-------------------------------------------------|
| `dirsize` | Show directory sizes including subdirectories.  |
| `fkill`   | Force kill processes by PID (like `kill -9`).   |
| `gpu-mon` | Real-time GPU process monitoring with `nvidia-smi pmon`. |
| `gpu-smi` | Quick snapshot of GPU usage (top lines).        |
| `pinfo`   | Show detailed information of a process by PID.  |
| `psx`     | Enhanced `ps` filtering by user and keyword.    |
| `up`      | Run shell scripts in background with logging.   |
| `watchx`  | Simplified wrapper for `watch -n 1 "<command>"`.|

---

## 🚀 Usage Examples

### dirsize
```bash
dirsize                # Show sizes in current directory
dirsize /path/to/dir
```

### fkill
```bash
fkill 12345            # Kill process with SIGKILL
```

### gpu-mon
```bash
gpu-mon                # Monitor GPU every second, defalut 12 rows
gpu-mon 8              # Optional: show top 8 lines  
```

### gpu-smi
```bash
gpu-smi                # Monitor GPU every second
```

### pinfo
```bash
pinfo 12345            # Show detailed info for process with PID 12345
```

### psx
```bash
psx                    # Show current user's processes
psx python             # Show current user's processes filtered by "python"
psx root ssh           # Show user root's processes filtered by "ssh"
```

### up
```bash
up script.sh           # Run script.sh in background, logging output to logs/script.log
```

### watchx
```bash
watchx nvidia-smi      # Run "nvidia-smi" every 1 second using watch
```


## Installation
1.Clone the repository
```bash
git clone https://github.com/shell-tools-lite/shell-tools-lite.git
```

2.Add `bin` directory to your PATH by adding this line to your shell config (`~/.bashrc` or `~/.zshrc`):
```bash
export PATH="$HOME/shell-tools-lite/bin:$PATH"
```

3.Reload your shell
```bash
source ~/.bashrc  # or source ~/.zshrc
```

