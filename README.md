# remote-job-submission-nci
Submit jobs to NCI supercomputer remotely. 

1-	Download/clone the wrapper scripts from NCI cloud GitHub repository. E.g. use your $HOME/bin folder

git clone https://github.com/NCI-Cloud/remote-job-submission-nci.git
 
2-	Add the repository to the $PATH e.g. for bash
Export PATH=$PATH:$HOME/bin/remote-job-submission-nci

3-	Create ssh key and enable passwordless ssh to NCI’s supercomputer using ssh-keygen
4-	Copy the key to the supercomputer. E.g. for Raijin
ssh-copy-id -i ~/.ssh/id_rsa.pub nciuserid@raijin.nci.org.au

5-	Use qstat, qsub and qdel to manage your jobs. Please note that all your scripts and data ‘must’ reside on NCI’s global filesystem. Data local to the virtual machine is not assessable to Raijin.
