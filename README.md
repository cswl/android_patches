### patches

instead of forking and merging, i like to maintain a linear history
so that the changes always apply to on top of the branch

this requires a little maintainence and fails on conflicts
but is a bit "cleaner"

### repos
https://github.com/galaxys1-nougat/android_bionic  
https://github.com/galaxys1-nougat/android_build  
https://github.com/galaxys1-nougat/android_frameworks_av  
https://github.com/galaxys1-nougat/android_frameworks_base   
https://github.com/galaxys1-nougat/android_hardware_ril  
https://github.com/galaxys1-nougat/android_system_core   

### usage
After a `repo sync` repo will checkout the branch from specified remote.  
Run `./patches/patch.sh log` from source dir to see if the original remote has updated.  
Then rebase with `./patches/patch.sh rebase`

Fix the patch upon confict if necessary.  
Then update our remote with  
`./patches/patch.sh forcepush