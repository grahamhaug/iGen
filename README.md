# iGen
iGen allows for interactive generation of Gaussian 16 input files (.com's) from .xyz's or .gjf's in a local directory.

Given a folder containing .xyz or .gjf (from GaussView) files, create G16 inputs interactively from the command line
<br />![image](https://user-images.githubusercontent.com/49004818/144347445-15486c9b-8640-4f93-a03b-85689fb8bb19.png)

Based on your choice of input files, iGen will locate all files in local directory. You can select a single .xyz/.gjf file to create an input for, a range (based on a keyword), or batch submission for all .xyz/.gjf's in current directory:
<br />![image](https://user-images.githubusercontent.com/49004818/144347719-b4b1b8a5-ebf7-47fa-a45a-85e65de3fd2f.png)

Depending on your workflow, your input files may have the same (ex: from CREST conformer generation) or different (ex: many structures over a project) charge/multiplicity.
You can save time by indicating that all files have the same charge/multiplicity: 
<br />![image](https://user-images.githubusercontent.com/49004818/144347918-6f53c3a9-1426-413d-abe6-a21e808eace5.png)

Alternatively, you can enter charge/multiplicty job-by-job for your selected inputs: 
<br />![image](https://user-images.githubusercontent.com/49004818/144348016-770888de-bc95-4625-91be-25344919d704.png)

Pick from a prepared menu of common job types: 
<br />![image](https://user-images.githubusercontent.com/49004818/144348189-0f92a049-2c7f-46fe-b324-f61033e9d52f.png)

Similarly, you can select from a menu of commonly-used DFA's and basis sets (these are easily customizable by editing the iGen functions corresponding to your specific DFA/dispersion/basis set/etc choices): 
<br />![image](https://user-images.githubusercontent.com/49004818/144348295-53bf82f8-a2c9-467c-9c8f-a83804fe83a9.png) 
<br />![image](https://user-images.githubusercontent.com/49004818/144348341-4f190a79-e118-481b-93e1-bfdf9417a790.png) 
<br />![image](https://user-images.githubusercontent.com/49004818/144348351-8438d11c-2f58-4df3-b55a-100042a998d9.png) 


You can also choose to use an implicit solvation model (either SMD or PCM) and select from a batch of solvents (these can be added easily, also): 
<br />![image](https://user-images.githubusercontent.com/49004818/144348434-26e67f86-aca4-4ab1-9d86-03d517197265.png)


Finally, you may choose which queue to submit the job on (this is system dependent and assumes your HPC is running with SLURM workload manager). 


Configuration is simple:
1. Add the iGen script and the G16_Input_Template.txt file to a Home/scripts directory
2. Use 'chmod 755 iGen' to make iGen executable
3. Add an alias to your bashrc for iGen: alias iGen='/yourpath/scripts/iGen'
4. in the iGen script, change the following line to point to your G16_Input_Template.txt location:
<br />![image](https://user-images.githubusercontent.com/49004818/144349025-ec17b821-0edc-4f14-b9da-edc56b620e25.png)
5. Call iGen from the command line
