# LAStSUccessRUN

lasurun is a simple script that:

- takes command name, executes it and return its exit code
- save the datetime of obtained exit code

It is useful for such situations:

- simple track of some app that lacks logging support
- you need to log only fails that occure not so often
- you need to know when the some service last worked successfully

It works under any OS that have Perl installed, no extra dependencies required. Script returns original exit code of executed command, so it can be integrated seamlessly into existing workflows.

## Usage

```

lasurun -l logfile [ options ] command to run

Options:

-l logfile    Write logged exit codes and time it occured to `logfile`
-n <int>      Keep last N records for each exit code. Default: 1
-c <codes>    Comma separated list of integer codes, that must be recorded. 
              By default all exit codes recorded

```
