# "Hands on" tutorial

## Before we begin ...

!SUB

![](images/escape_to_athena_2.png)<!-- .element width="40%" -->

<small>[* letterboxd.com/film/escape-to-athena](https://letterboxd.com/film/escape-to-athena/)</small>

!SUB

**Let's obtain jupyter-lab notebook on Cyfronet's Athena**

```
[laptop]$ ssh plg...@athena.cyfronet.pl
```

```
[athena]$ ln -s $SCRATCH scratch
[athena]$ ln -s $PLG_GROUPS_STORAGE group
```

```
[athena]$ cp group/tutorial/python-notebook.slurm $HOME
```

```
[athena]$ cat python-notebook.slurm
[athena]$ sbatch python-notebook.slurm
[athena]$ hpc-jobs
```

```
[athena]$ ls | grep jupyter-log-

and use the one with the highest number in the following commands
```

```
In a new terminal window on your laptop execute output of the following command:

[athena]$ grep "ServerAliveInterval" jupyter-log-nnnnnn.txt
```

```
Execute the following command:

[athena]$ grep "127.0.0.1" jupyter-log-nnnnnn.txt | grep "token" | grep -v ServerApp

-> on your laptop go to the address obtained
```

!SUB

## Athena

### Useful commands

```
* hpc-grants - shows available grants, resource allocations

* hpc-fs - shows available storage

* hpc-jobs - shows currently pending/running jobs

* hpc-jobs-history - shows information about past jobs
```

### Storage

```
* $HOME    /net/people/plgrid/<login>

* $SCRATCH    /net/tscratch/people/<login>

* $PLG_GROUPS_STORAGE/plggeurocctt    /net/pr2/projects/plgrid/plggeurocctt
```

<!--
!SUB
### Visual Studio Code + Git

![VSC start](images/vsc-start.png)
-->

</br>

<small>[Athena - Maciej Pawlik - Confluence](https://docs.cyfronet.pl/display/~plgpawlik/Athena)</small>
