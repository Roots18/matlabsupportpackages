This is a guide for installing previously downloaded support software.

Table of Contents
-----------------

1. Copy downloaded software
2. Interactive Installation
    a. Windows
    b. Linux
    c. Mac
3. Silent Installation
    a. Windows
    b. Linux
    c. Mac

1. Copy downloaded software
---------------------------

    Copy this entire folder to a shared network drive or removable media and then access the
    copied folder from the computer on which you want to run the installation.

2. Interactive Installation
---------------------------

    The interactive installer will start MATLAB and then the installer in a separate window. The
    executable takes a single argument; the path to the location of the previously downloaded
    files. All available support packages in the specified download folder are presented.

    In a command prompt, type the following:

    a. Windows

        cd DRIVE:\<MATLAB_PATH>\bin\win64
        install_supportsoftware.exe -archives <path_to_download_folder> [-matlabroot DRIVE:\MATLAB_PATH]

        For example:

        cd C:\MATLAB\R2018b\bin\win64
        install_supportsoftware.exe -archives C:\Users\jsmith\Downloads\MathWorks\SupportPackages\R2018b\

    b. Linux

        cd <MATLAB_PATH>/bin/glnxa64
        ./install_supportsoftware.sh -matlabroot <MATLAB_PATH> -archives <path_to_download_folder>

        For example:

        cd /opt/MATLAB/R2018b/bin/glnxa64
        ./install_supportsoftware.sh -matlabroot /opt/MATLAB/R2018b -archives /home/jdoe/Downloads/MathWorks/SupportPackages/R2018b

    b. Mac

        cd <MATLAB_PATH>/bin/maci64
        ./install_supportsoftware.sh -matlabroot <MATLAB_PATH> -archives <path_to_download_folder>

        For example:

        cd /Applications/MATLAB_R2018b.app/bin/maci64
        ./install_supportsoftware.sh -matlabroot /Applications/MATLAB_R2018b.app/ -archives /Users/jdoe/Downloads/MathWorks/SupportPackages/R2018b


3. Silent Installation
----------------------

    NOTE: The silent installation of support packages is only available in MATLAB releases R2018a
    and newer. For MATLAB releases before R2018a, see the interactive installation instructions.

    The silent installer executable takes two arguments; a path to the location of the previously
    downloaded files and the location of the input file. The input file is used to specify the
    support packages that are to be installed.

    In a command prompt, type the following:

    a. Windows

        cd DRIVE:\<MATLAB_PATH>\bin\win64
        SupportSoftwareInstaller.exe -downloadfolder <path_to_download_folder> -inputfile <path_to_input_file>\ssi_input.txt

        For example:

        cd C:\MATLAB\R2018b\bin\win64
        SupportSoftwareInstaller.exe -downloadfolder C:\Users\jsmith\Downloads\MathWorks\SupportPackages\R2018b -inputfile C:\Users\jsmith\Downloads\MathWorks\SupportPackages\R2018b\ssi_input.txt

    b. Linux

        cd <MATLAB_PATH>/bin/glnxa64
       ./SupportSoftwareInstaller -downloadfolder <path_to_download_folder> -inputfile <path_to_input_file>/ssi_input.txt

        For example:

        cd /opt/MATLAB/R2018b/bin/glnxa64
        ./SupportSoftwareInstaller.sh -downloadfolder /home/jdoe/Downloads/MathWorks/SupportPackages/R2018b -inputfile /home/jdoe/Downloads/MathWorks/SupportPackages/R2018b/ssi_input.txt

    c. Mac

       cd <MATLAB_PATH>/bin/maci64
       ./SupportSoftwareInstaller.sh -downloadfolder <path_to_download_folder> -inputfile <path_to_input_file>/ssi_input.txt

       For example:

       cd /Applications/MATLAB_R2018b.app/bin/maci64
       ./SupportSoftwareInstaller.sh -downloadfolder /Users/jdoe/Downloads/MathWorks/SupportPackages/R2018b -inputfile /Users/jdoe/Downloads/MathWorks/SupportPackages/R2018b/ssi_input.txt