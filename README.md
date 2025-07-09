# Ping Monitor

A simple Python script that checks the availability of IP addresses or domain names and generates a color-coded Excel report.

---

## Features

- Reads hostnames/IPs from a plain text file (`hosts.txt`)
- Pings each host using the `ping3` library
- Logs status as `OK`, `OFFLINE`, or `PING ERROR`
- Captures exact date and time of each check
- Generates a `.xlsx` file with a table of results
- Highlights rows in green for OK or red for OFFLINE

---

## Requirements

- Python 3.7+
- `ping3`
- `openpyxl`

Install dependencies:

```bash
pip install ping3 openpyxl
```

---

## How to Use

Follow these steps to run the project locally:

### 1. Clone the repository

```bash
git clone https://github.com/your-username/ping-monitor.git
cd ping-monitor
```

### 2. Install required libraries

```bash
pip install ping3 openpyxl
```

### 3. Add hosts to `hosts.txt`

Each line should contain one host (domain or IP address):

```
8.8.8.8
google.com
localhost
192.168.3.1
```

### 4. Run the script

```bash
python ping_report.py
```

### 5. View the output

Open the generated file `report.xlsx` using Excel, Numbers, or LibreOffice.

---

## Example Output

| Host         | Status   | Date       | Time     |
|--------------|----------|------------|----------|
| 8.8.8.8      | OK       | 2025-07-08 | 21:02:23 |
| google.com   | OK       | 2025-07-08 | 21:02:24 |
| 192.168.3.10 | OFFLINE  | 2025-07-08 | 21:02:25 |

 Green rows = reachable hosts  
 Red rows = unreachable hosts


---

## Project Structure

```
ping_monitor/
├── ping_report.py      # Main script
├── hosts.txt           # List of hosts to ping
├── report.xlsx         # Auto-generated output (ignored by git)
├── .gitignore          # Git ignore rules
└── README.md           # This file
```

---

## Author

**Mateusz Gala**  
Computer Science student passionate about automation, scripting and IT infrastructure.

- Engineering student (3 semesters left)  
- Builds real-world tools and improves through projects  
- Communicative, curious, and not afraid to ask questions

---

## Future Improvements

- [ ] Send report via email automatically
- [ ] Schedule repeated pings using `cron` or `schedule`
- [ ] Store ping history for each host
- [ ] Add CLI options for configuration
- [ ] Create a web dashboard to display live status

---

## Why This Project?

This project combines network diagnostics, scripting, data handling, and reporting — practical skills applicable in IT support, DevOps, and automation roles. It also serves as a portfolio project to demonstrate clean code, documentation, and result presentation.
