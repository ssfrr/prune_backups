prune_backups
=============

Prunes/thins your backups within different ranges. For instance you may want to
keep daily backups for the past week, weekly backups for the past month, and
monthly backups for the past year.

Usage:
    prune_backups [--rm] [--pattern=PATTERN] [--quiet] <freqs>...

Options:
    --rm                Actually remove the backups. By default it just prints
                        a list of files to remove
    --pattern=PATTERN   The file pattern to match for your backups.
                        [default: ./*]
    --quiet             Suppress output unless there's a problem
    <freqs>             A list of intervals in days, e.g. `prune_backups 1 7
                        30` would keep daily backups for the first 7 days,
                        weekly backups for the first 30, and every 30 days
                        after that.
