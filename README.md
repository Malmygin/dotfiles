- config in commit "init repo" for HP 6730b
	- sync package:
		- create file install package `pacman -Qqe > pkglist.txt`
		- for auto sync create /etc/pacman-update:
			```bash
			[Trigger]
			Operation = Install
			Operation = Remove
			Type = Package
			Target = *

			[Action]
			When = PostTransaction
			Exec = /bin/sh -c '/usr/bin/pacman -Qqe > /etc/pkglist.txt
			```
						


