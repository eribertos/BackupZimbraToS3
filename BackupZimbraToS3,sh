#!/bin/bash -x
Dia=$(date +%d-%m-%Y)


echo $Dia > /opt/zimbra/backup/lista.txt


mkdir /mnt/s3/Backup-zimbra-$(cat /opt/zimbra/backup/lista.txt)




for i in $(/opt/zimbra/bin/zmprov -l gaa);do

        /opt/zimbra/bin/zmmailbox -z -m $i gru "///?fmt=tgz" > /mnt/s3/Backup-zimbra-$(cat /opt/zimbra/backup/lista.txt)/$i.tgz

done
