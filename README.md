# Travis CI to upload to an FTP server
## About
This is a lightweight Travis CI FTP upload client which triggers a generic JS console log script, and then pushes all changed files to the FTP server. Currently, this will reupload all files rather than selectively uploading changed files (ergo, is not 100% efficient).

## Usage
- Pull the repository, and insert your files for FTP upload (e.g. website) into the same folder.
- Modify deploy.sh to reflect your FTP address
- Setup your repo on Travis CI (travis-ci.org)
- On Travis CI, make secure environment variables called FTP_USER and FTP_PASS under SETTINGS --> ENVIRONMENT VARIABLES, representing your FTP login credentials
- On pushing the repo to GitHub, Travis CI should now take over, and start uploading your files to your FTP server. Dependent on size, this can take up to 15 mins.

## Issues
- Selectively uploading files rather than re-uploading the whole repository (free tier FTP servers have limited data usage)
