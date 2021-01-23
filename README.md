### Gather subdomains from cidr
while read line; do mapcidr -cidr $line -silent | dnsx -silent -ptr -resp-only | tee -a hosts; done<cidr.txt

-----------------------------

### Masscan with common nmap ports
~/masscan/bin/masscan -iL ip --rate 1000 -oJ masscan_output.json -p 10000,1080,1100,1241,1352,1433,1434,1521,15672,161,1944,2301,3000,30821,3128,3306,3366,3868,4000,4001,4002,4040,4044,4100,443,4433,457,5000,5673,5801,5802,5900,6000,6346,6347,66,7001,7002,7077,7080,7443,7447,80,8000,8008,8080,8081,8089,81,8181,8443,8880,8888,8983,9000,9091,9443,9999
