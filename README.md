### Gather subdomains from cidr
while read line; do mapcidr -cidr $line -silent | dnsx -silent -ptr -resp-only | tee -a hosts; done<cidr.txt
