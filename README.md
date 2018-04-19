# ep_fileupload_aws

Clone of ep_fileupload, however it uploads to AWS S3 instead of using the file system. 

    /*Add to your settings file*/
    "ep_fileupload_aws" : {
       "S3_ACCESS_KEY": "YOUR_ACCESS_KEY",
       "S3_SECRET_KEY":"YOUR_SECRET_KEY",
       "bucket" : "BUCKET_NAME",
       "base_key" : "PREPEND YOUR KEY WITH THIS", /* usually a folder, something like "folder/subfolder/" */
    }

Uploaded files will be given a GUID, the GUID will function as the file identifier in AWS and in Etherpad.

The plugin plays nice with ep_fileupload's urls. You'd just need to copy your existing files your S3 bucket. The pad URL's will correctly redirect.

**NOTICE: Make a backup of your files! **

Removing "ep_fileupload" on etherpad will delete any uploaded files from your server. Copy your files before replacing "ep_fileupload" with "ep_fileupload_aws".

ep_fileupload stores files in the  node_modules/ep_fileupload/upload folder
