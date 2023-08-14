# Emacs Unofficial Patches

Created: 1999/11/29, Revised: 2003/01/14

There are [Emacs](http://www.gnu.org/software/emacs/emacs.html)
unofficial patches,
provided by the author **AS IS** and any express
or implied warranties are disclaimed.

***
## MULE 4.1-ized

> [!IMPORTANT]
> Announced on 2001/09/01
>
> A bug of `decode-coding-string<f>` is present in MULE 4.1.
Therefore, I recommend upgrading to
[Emacs 20.7 with new patch](emacs-20.7-mule-4.1b.patch).
I am very sorry for having caused you inconvenience.
> 
> Note that this problem was not present in (original) MULE 4.0
or MULE 5.0.

There are unofficial patches
for Emacs 20.\* (20.4 or later, but except 21.\*) with MULE 4.0
to upgrade Emacs 20.\* with MULE 4.1, the feature came from Meadow 1.10.

- UTF-8 and UTF-16 autodetection.
- `make-coding-system<f>` have a new optional argument EOL-TYPE.

In this context,
MULE stands for *Multilingal Environment*,
not *MULtilingal enhancement to GNU Emacs*.

- for Emacs 20.4
	- [emacs-20.4-mule-4.1.patch](emacs-20.4-mule-4.1.patch)
- for Emacs 20.4.91
	- [emacs-20.4.91-mule-4.1.patch](emacs-20.4.91-mule-4.1.patch)
- for Emacs 20.4.92
	- [emacs-20.4.92-mule-4.1.patch](emacs-20.4.92-mule-4.1.patch)
- for Emacs 20.4.93
	- [emacs-20.4.93-mule-4.1.patch](emacs-20.4.93-mule-4.1.patch)
- for Emacs 20.5
	- [emacs-20.5-mule-4.1.patch](emacs-20.5-mule-4.1.patch)
	(This patch can be applied for both of Emacs 20.5 and Emacs 20.5a.)
- for Emacs 20.5.90
	- [emacs-20.5.90-mule-4.1.patch](emacs-20.5.90-mule-4.1.patch)
- for Emacs 20.5.91
	- [emacs-20.5.91-mule-4.1.patch](emacs-20.5.91-mule-4.1.patch)
- for Emacs 20.6
	- [emacs-20.6-mule-4.1.patch](emacs-20.6-mule-4.1.patch)
- for Emacs 20.6.90
	- [emacs-20.6.90-mule-4.1.patch](emacs-20.6.90-mule-4.1.patch)
- for Emacs 20.6.92
	- [emacs-20.6.92-mule-4.1.patch](emacs-20.6.92-mule-4.1.patch)
- for Emacs 20.7
	- ~~[emacs-20.7-mule-4.1.patch](emacs-20.7-mule-4.1.patch)~~
	(Use new patch below.
	This patch contains a bug of `decode-coding-string<f>`.)
	- ~~[emacs-20.7-mule-4.1a.patch](emacs-20.7-mule-4.1a.patch)~~
	(This patch includes "the fix of CCL interpretor",
	see next section for more information.)
	- [emacs-20.7-mule-4.1b.patch](emacs-20.7-mule-4.1b.patch)
	(No visible changes; corrected patch against previous one.)

## MULE 4.1-ized + the fix of CCL interpretor

The following patches contains
"the fix of CCL interpretor (some problem on MapMultiple instraction)"
with author's permission.
This fix made by Miyashita Hisashi who also known as "himi".
The original patch file can be found in Mule-UCS 0.80.

- for Emacs 20.6
	- [emacs-20.6-mule-4.1ext.patch](emacs-20.6-mule-4.1ext.patch)
- for Emacs 20.6.92
	- [emacs-20.6.92-mule-4.1ext.patch](emacs-20.6.92-mule-4.1ext.patch)
- for Emacs 20.7
	- ~~[emacs-20.7-mule-4.1.patch](emacs-20.7-mule-4.1.patch)~~
	(Use new patch below.
	This patch contains a bug of `decode-coding-string<f>`.)
	- ~~[emacs-20.7-mule-4.1a.patch](emacs-20.7-mule-4.1a.patch)~~
	(This patch includes "the fix of CCL interpretor".)
	- [emacs-20.7-mule-4.1b.patch](emacs-20.7-mule-4.1b.patch)
	(No visible changes; corrected patch against previous one.)

### Known Problems

1. with w3-4.0pre.46  
w3-4.0pre.46 do not work in Emacs 20.\* with MULE 4.1,
please apply [this patch](w3-4.0pre.46-mule-sysdp.el.patch) to fix.  
(made by Kyotaro HORIGUCHI and KOSEKI Yoshinori in meadow-develop)

1. with emcws  
I heard that couldn't build Emacs 20.\* with MULE 4.1 and emcws, sorry.

1. to build as NTemacs (not well tested)  
If you want to build Emacs 20.7 with MULE 4.1 (as NTemacs),
please apply [this patch](emacs-20.7-mule-4.1-nt.patch) before compile.  
(reported by KOSEKI Yoshinori in meadow-users-jp)

***
## Emacs 20.3 on BSD/OS 4.0

- for Emacs 20.3
	- [emacs-20.3-bsdi4.0.patch](emacs-20.3-bsdi4.0.patch)
