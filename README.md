# wmic

Make WMI queries against your Windows infrastructure from a Docker container.

wmic is from the Samba project, version 4.

## Instructions

`docker run cdrx/wmic //windows-host "select * from Win32_ComputerSystem"`

## wmic manual

```
NAME
       wmic - WMI client

SYNOPSIS
       [-?|--help]  [--usage]  [-d|--debuglevel  DEBUGLEVEL]  [--debug-stderr]
       [-s|--configfile CONFIGFILE]  [--option=name=value]  [-l|--log-basename
       LOGFILEBASE]  [--leak-report]  [--leak-report-full]  [-R|--name-resolve
       NAME-RESOLVE-ORDER] [-O|--socket-options SOCKETOPTIONS]
       [-n|--netbios\[u2010] name    NETBIOSNAME]    [-W|--workgroup
       WORKGROUP]   [--realm=REALM] [-i|--scope   SCOPE]    [-m|--maxprotocol
       MAXPROTOCOL]    [-U|--user [DOMAIN]USERNAME[%PASSWORD]]     [-N|--no-
       pass]     [--password=STRING] [-A|--authentication-file    FILE]
       [-S|--signing    on|off|required] [-P|--machine-pass]
       [--simple-bind-dn=STRING]  [-k|--kerberos  STRING]
       [--use-security-mechanisms=STRING] [-V|--version]  [--namespace=STRING]
       //host query

EXAMPLE
       Example: wmic -U [domain/]adminuser%password //host "select * from
       Win32_ComputerSystem"

DESCRIPTION
       --namespace=STRING
              WMI namespace, default to root\cimv2

   Help options:
       -?, --help
              Show this help message

       --usage
              Display brief usage message

   Common samba options:
       -d, --debuglevel=DEBUGLEVEL
              Set debug level

       --debug-stderr
              Send debug output to STDERR

       -s, --configfile=CONFIGFILE
              Use alternative configuration file

       --option=name=value
              Set smb.conf option from command line

       -l, --log-basename=LOGFILEBASE
              Basename for log/debug files

       --leak-report
              enable talloc leak reporting on exit

       --leak-report-full
              enable full talloc leak reporting on exit

   Connection options:
       -R, --name-resolve=NAME-RESOLVE-ORDER
              Use these name resolution services only

       -O, --socket-options=SOCKETOPTIONS
              socket options to use

       -n, --netbiosname=NETBIOSNAME
              Primary netbios name

       -W, --workgroup=WORKGROUP
              Set the workgroup name

       --realm=REALM
              Set the realm name

       -i, --scope=SCOPE
              Use this Netbios scope

       -m, --maxprotocol=MAXPROTOCOL
              Set max protocol level

   Authentication options:
       -U, --user=[DOMAIN\]USERNAME[%PASSWORD]
              Set the network username

       -N, --no-pass
              Don't ask for a password

       --password=STRING
              Password

       -A, --authentication-file=FILE
              Get the credentials from a file

       -S, --signing=on|off|required
              Set the client signing state

       -P, --machine-pass
              Use stored machine account password (implies -k)

       --simple-bind-dn=STRING
              DN to use for a simple bind

       -k, --kerberos=STRING
              Use Kerberos

       --use-security-mechanisms=STRING
              Restricted list of authentication mechanisms available for use
              with this authentication

   Common samba options:
       -V, --version
              Print version

EXAMPLE
       wmic -U [domain/]adminuser%password //host "select * from
       Win32_ComputerSystem"

AUTHOR
       This manual page was written by Bernd Zeimetz <bzed@debian.org> for the
       Debian project (but may be used by others).

```
