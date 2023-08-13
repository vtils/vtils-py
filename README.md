## VTILS

### Utility functions from VTILS  

  
  from vtils.util import Cipher  
  cipher = Cipher(key_text)  
  t1 = cipher.encrypt(plain_text)  
  t2 = cipher.decrypt(t1)  


### Encrypt File 

  
  from vtils.util import FileUtils
  svc = FileUtils(key_text)
  svc.encrypt_file(src, dest)


### Decrypt File  

  
  from vtils.util import FileUtils
  svc = FileUtils(key_text)
  svc.decrypt_file(src, dest)


## AWS Cloud Utils (AwsCloudtils) 

### Upload File  

  from vtils.cloud import AwsCloudtils
  svc = AwsCloudtils(accesskey, secretkey)
  success = svc.upload_file(src, s3bucket)
  if not success:
    print('Failed to upload file to s3 bucket')


### Download File  

  from vtils.cloud import AwsCloudtils
  svc = AwsCloudtils(accesskey, secretkey)
  success = svc.download_file(s3bucket, objname, dest)
  if not success:
    print('Failed to download file from s3 bucket')




