# Documentation
## Using Git LFS
I used Git LFS to store large data.
1. download git lfs from the official website
2. run `git lfs install`
3. before commiting any large fails in your repo run `git lfs track"*.mp4"` to specify what files to track
4. add the .gitattributes file to ur repo that was created `git add .gitattributes`
5. add the large files to your repo
6. commit and push your changes
7. if github still tries to upload your large data and you get an error try: `git lfs migrate import --include="*.mp4"` to migrate old large files.
> Reason for error is that lfs needs to start tracking the files before it was ever added or commited. If there are already existing large files you want to upload to lfs then try `7.`