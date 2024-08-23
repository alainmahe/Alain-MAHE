# Alain-MAHE
Error BARMAN Backup
[barman@MyPC ~]$  barman --debug backup MySERVUR
WARNING: No backup strategy set for server 'MySERVUR' (using default 'concurrent_backup').
Starting backup using rsync-concurrent method for server MySERVUR in /rep/MySERVUR/base/20240822T164924
DEBUG: detecting data directory
DEBUG: detecting tablespaces
Backup start at LSN: 245/D1000028 (0000000100000245000000D1, 00000028)
This is the first backup for server MySERVUR
ERROR: The backup has failed starting backup
Asking PostgreSQL server to finalize the backup.
DEBUG: Writing backup label: /rep/MySERVUR/base/20240822T164924/data/backup_label
ERROR: Backup failed writing backup label.
DETAILS: [Errno 2] No such file or directory: '/rep/MySERVUR/base/20240822T164924/data/backup_label'
DEBUG: Starting archive-wal for server MySERVUR
Processing xlog segments from file archival for MySERVUR
        0000000100000245000000D0
        0000000100000245000000D1
        0000000100000245000000D1.00000028.backup
EXCEPTION: [Errno 5] Input/output error: '/rep/MySERVUR/wals/tmpe2xeiv3w'
See log file for more details.


2024-08-22 15:47:01,512 [2833677] barman.config WARNING: Discarding configuration file: .barman.auto.conf (not a file)
2024-08-22 15:47:01,528 [2833677] barman.backup_executor WARNING: No backup strategy set for server 'MySERVUR' (using default 'concurrent_backup').
2024-08-22 15:47:01,628 [2833677] barman.utils INFO: Cleaning up lockfiles directory.
2024-08-22 15:47:01,743 [2833678] barman.config WARNING: Discarding configuration file: .barman.auto.conf (not a file)
2024-08-22 15:47:01,757 [2833678] barman.backup_executor WARNING: No backup strategy set for server 'MySERVUR' (using default 'concurrent_backup').
2024-08-22 15:47:01,781 [2833678] barman.wal_archiver INFO: Found 6 xlog segments from file archival for MySERVUR. Archive all segments in one run.
2024-08-22 15:47:01,782 [2833678] barman.wal_archiver INFO: Archiving segment 1 of 6 from file archival: MySERVUR/0000000100000245000000C3
2024-08-22 15:47:02,135 [2833678] barman.wal_archiver INFO: Archiving segment 2 of 6 from file archival: MySERVUR/0000000100000245000000C4
2024-08-22 15:47:02,498 [2833678] barman.wal_archiver INFO: Archiving segment 3 of 6 from file archival: MySERVUR/0000000100000245000000C4.00000028.backup
2024-08-22 15:47:02,559 [2833678] barman.wal_archiver INFO: Archiving segment 4 of 6 from file archival: MySERVUR/0000000100000245000000C5
2024-08-22 15:47:02,897 [2833678] barman.wal_archiver INFO:     Error: 0000000100000245000000C5 is already present in server MySERVUR. File moved to errors directory.
2024-08-22 15:47:02,943 [2833678] barman.wal_archiver INFO: Archiving segment 5 of 6 from file archival: MySERVUR/0000000100000245000000C6
2024-08-22 15:47:03,306 [2833678] barman.wal_archiver INFO: Archiving segment 6 of 6 from file archival: MySERVUR/0000000100000245000000C7
2024-08-22 15:47:03,841 [2833678] barman.wal_archiver WARNING: Archiver is about to move 1 unexpected file(s) to errors directory for MySERVUR from file archival
2024-08-22 15:47:03,841 [2833678] barman.wal_archiver WARNING: Moving unexpected file for MySERVUR from file archival: archive_status
2024-08-22 15:47:07,737 [2833699] barman.config WARNING: Discarding configuration file: .barman.auto.conf (not a file)
2024-08-22 15:47:07,752 [2833699] barman.backup_executor WARNING: No backup strategy set for server 'MySERVUR' (using default 'concurrent_backup').
2024-08-22 15:47:09,604 [2833699] barman.server INFO: Ignoring failed check 'failed backups' for server 'MySERVUR'
2024-08-22 15:47:10,325 [2833699] barman.server INFO: Ignoring failed check 'archiver errors' for server 'MySERVUR'
2024-08-22 15:47:10,420 [2833699] barman.backup INFO: Starting backup using rsync-concurrent method for server MySERVUR in /rep/MySERVUR/base/20240822T154710
2024-08-22 15:47:10,597 [2833699] barman.backup_executor INFO:  16400, fib_data, /pg_tblspce
2024-08-22 15:47:11,059 [2833699] barman.backup_executor INFO: Backup start at LSN: 245/C6000028 (0000000100000245000000C6, 00000028)
2024-08-22 15:47:11,065 [2833699] barman.backup_executor INFO: This is the first backup for server MySERVUR
2024-08-22 15:47:11,089 [2833699] barman.backup_executor ERROR: The backup has failed starting backup
2024-08-22 15:47:11,089 [2833699] barman.backup_executor INFO: Asking PostgreSQL server to finalize the backup.
2024-08-22 15:47:14,738 [2833699] barman.backup ERROR: Backup failed writing backup label.
DETAILS: [Errno 2] No such file or directory: '/rep/MySERVUR/base/20240822T154710/data/backup_label'
2024-08-22 15:47:14,814 [2833699] barman.wal_archiver INFO: Found 3 xlog segments from file archival for MySERVUR. Archive all segments in one run.
2024-08-22 15:47:14,814 [2833699] barman.wal_archiver INFO: Archiving segment 1 of 3 from file archival: MySERVUR/0000000100000245000000C5
2024-08-22 15:47:15,152 [2833699] barman.wal_archiver INFO:     Error: 0000000100000245000000C5 is already present in server MySERVUR. File moved to errors directory.
2024-08-22 15:47:15,190 [2833699] barman.wal_archiver INFO: Archiving segment 2 of 3 from file archival: MySERVUR/0000000100000245000000C6
2024-08-22 15:47:15,500 [2833699] barman.wal_archiver INFO:     Error: 0000000100000245000000C6 is already present in server MySERVUR. File moved to errors directory.
2024-08-22 15:47:15,550 [2833699] barman.wal_archiver INFO: Archiving segment 3 of 3 from file archival: MySERVUR/0000000100000245000000C6.00000028.backup
2024-08-22 15:47:15,693 [2833699] barman.cli ERROR: [Errno 5] Input/output error: '/rep/MySERVUR/wals/tmp5yu_x5bi'
See log file for more details.
Traceback (most recent call last):
  File "/usr/lib/python3.6/site-packages/barman/cli.py", line 2390, in main
    args.func(args)
  File "/usr/lib/python3.6/site-packages/barman/cli.py", line 546, in backup
    backup_name=args.backup_name,
  File "/usr/lib/python3.6/site-packages/barman/server.py", line 1651, in backup
    self.backup_manager.remove_wal_before_backup(backup_info)
  File "/usr/lib/python3.6/site-packages/barman/backup.py", line 1259, in remove_wal_before_backup
    with tempfile.TemporaryFile(mode="w+", dir=xlogdb_dir) as fxlogdb_new:
  File "/usr/lib64/python3.6/tempfile.py", line 624, in TemporaryFile
    _os.unlink(name)
OSError: [Errno 5] Input/output error: '/rep/MySERVUR/wals/tmp5yu_x5bi'
