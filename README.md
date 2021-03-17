**Windows command-line prompt**

ToC
[toc]


# PROMPT variable
By default, the windows command-line prompt is defined as `$P$G` in the `PROMPT` variable. This translates to current drive and path with a greater-than sign suffix. 


## Configurations

**Default**

	SET PROMPT=$P$G

**Path\n\nPrompt**

	SET PROMPT=$P$_$_$+$G

**User@Password\nPath\n\nPrompt**

	SET PROMPT=%USERNAME%@%COMPUTERNAME%$_$P$_$_$+$G

**User@Password\nPath\nNetwork path\n\nPrompt**

	SET PROMPT=%USERNAME%@%COMPUTERNAME%$_$P$_$M$_$_$+$G

**User@Password\nPath\nNetwork path\nDate+T+Time\n\nPrompt**

	SET PROMPT=%USERNAME%@%COMPUTERNAME%$_$P$_$M$_$DT$T$_$_$+$G


### Use in a shortcut
For this to be used in a shortcut, we can use the following command in the `Shortcut` tab, and then `Target` field.

	C:\Windows\system32\cmd.exe /k "SET PROMPT=<CFG>"

The `<CFG>` is any of the above configurations.