# teleportinfolabels
Scripts and howtos for providing resource information and with easily identifable colors.

Example:
![image](https://user-images.githubusercontent.com/60704961/153775157-e6dac8dd-e92f-4286-8fd0-3e0581e70616.png)


WARNING: Confirm any of these scripts prior to use. All of them should be non-impactful. If you configure with a low period level that may cause additional overhead on the machine.

You can call a program or script program.  In addition to 

## Node Information

Script files:
- `getnodeinfo.sh`
- `getfreemem.sh`
- `getfreespace.sh`

Example `getnodeinfo.sh` output that combines the `getfreemem.sh` and `getfreespace.sh` output.
stats: 25% mem 🟢 54% storage 🟡

To install:
1. Retrieve this repository
2. Add `getnodeinfo.sh`, `getfreemem.sh`, `getfreespace.sh` to user running Teleport's path or 
   copy to `/usr/local/bin`
3. Confirm output running
```bash
getnodeinfo.sh
```


```yaml
ssh_service:
  enabled: yes
  labels:
    env: prod
  commands:
  - command:
    - getnodeinfo.sh
    name: stats
    period: 1m
```




