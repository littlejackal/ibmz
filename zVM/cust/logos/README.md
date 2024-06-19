# z/VM System Logos

![JKLVM](image/JKLVM.jpg)

FTP to VM -- must set type E and mode B!!

``` 
230-MAINT logged in; working directory = MAINT 191 (ReadOnly)
ftp> quote type e
ftp> quote mode b
ftp> put JLKVM.INPTAREA
ftp> put JKLVM.LOGO
```

Then relocate to PARMDISK CF1

```
cprel a
link maint cf1 cf1 mr
acc cf1 z
copy JKLVM * A = = Z
```
