# Linux System Monitor

A real-time system monitoring tool for Linux built in C++ - similar to `htop` and `top`.

![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=c%2B%2B&logoColor=white)

## Features

- 📊 Real-time CPU and memory usage with progress bars
- 📋 Process monitoring (PID, user, CPU%, RAM, runtime)
- 🔄 Auto-refresh every second
- ⚡ Lightweight and fast

## Screenshots

<p align="center">
  <img src="images/Screenshot_2025-11-08_12_34_48.png" width="45%" alt="Main Interface"/>
  <img src="images/Screenshot_2025-11-08_12_35_34.png" width="45%" alt="CPU Usage"/>
</p>

<p align="center">
  <img src="images/Screenshot_2025-11-08_12_35_43.png" width="45%" alt="Process List"/>
  <img src="images/Screenshot_2025-11-08_12_35_49.png" width="45%" alt="Live Monitor"/>
</p>

## Installation

```bash
# Install dependencies
sudo apt update
sudo apt install build-essential libncurses5-dev libncursesw5-dev make -y

# Clone and build
git clone https://github.com/rnxtremer/System_Monitor-Linux.git
cd System_Monitor-Linux
make build

# Run
./build/monitor
```

## Usage

- **Run**: `./build/monitor`
- **Quit**: Press `q`
- **Root access** (optional): `sudo ./build/monitor`

## How It Works

Reads data from Linux `/proc` filesystem:
- `/proc/stat` - CPU statistics
- `/proc/meminfo` - Memory info
- `/proc/[PID]/stat` - Process stats

## Project Structure

```
System_Monitor-Linux/
├── include/        # Header files
├── src/           # Source files
├── images/        # Screenshots
├── build/         # Build output
├── Makefile       # Build config
└── README.md      # This file
```

## Commands

```bash
make build    # Compile
make clean    # Remove build files
make debug    # Build with debug symbols
```

## Troubleshooting

- **ncurses not found**: `sudo apt install libncurses5-dev`
- **Permission denied**: Run with `sudo ./build/monitor`
- **Compilation errors**: `make clean && make build`

## Author

**rnxtremer** - [GitHub](https://github.com/rnxtremer)

## License

MIT License - Open source and free to use

---

⭐ If you find this useful, please star the repo!
