# Bash Scripting Suite for System Maintenance

## Overview
This repository contains a suite of Bash scripts to automate common Linux system maintenance tasks: backups, updates/cleanup, log monitoring, and system reporting. It includes an interactive menu and sample cron integration instructions.

## How to use
1. Make scripts executable:
   ```bash
   chmod +x *.sh
   ```
2. (Optional) Run installer:
   ```bash
   sudo ./install.sh
   ```
3. Run interactive menu:
   ```bash
   sudo ./maintenance_menu.sh
   ```
4. Or run individual scripts:
   ```bash
   sudo ./backup.sh /home
   sudo ./update_cleanup.sh
   ./log_monitor.sh
   ./user_reports.sh
   ```

## Files
- backup.sh
- update_cleanup.sh
- log_monitor.sh
- user_reports.sh
- maintenance_menu.sh
- install.sh
- Capstone_Project_Report_AbhishekKumarGourav.pdf
- screenshots/ (placeholders)

## Cron examples
```bash
0 2 * * * /usr/bin/env bash /opt/maint_suite/backup.sh /home >> /var/log/maint_suite/cron_backup.log 2>&1
0 4 * * 0 /usr/bin/env bash /opt/maint_suite/update_cleanup.sh >> /var/log/maint_suite/cron_update.log 2>&1
*/30 * * * * /usr/bin/env bash /opt/maint_suite/log_monitor.sh >> /var/log/maint_suite/cron_logmonitor.log 2>&1
```
