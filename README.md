#!/bin/bash

now=`date`

time=`echo $now | awk '{printf $5}' | awk 'BEGIN{FS=":"}{printf $1}'`

#We can also define a variable:time,with the value of "date +%H"

if [ "$time" -ge "0" -a "$time" -lt "12" ]
then
        str="morning"

elif [ "$time" -ge "12" -a "$time" -lt "18" ]
then
        str="afternoon"

else
        str="evening"
fi

echo "Good $str"
