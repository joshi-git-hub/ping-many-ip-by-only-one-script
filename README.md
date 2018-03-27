# ping-many-ip-by-only-one-script
#this script is basically for pinging many ip addresses so we could check which one is up or down.
#!/bin/bash
for i in 192.168.2.{1..150}
do
ping -c 2 $i >> /dev/null
if [ $? -eq 0 ]
then
  echo "$i is up."
else
 echo "$i is down."
fi
done
