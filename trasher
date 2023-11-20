#!/bin/bash
if [[ $# -ne 1 ]]
then
	echo “usage: $0 arg1 file0,file1,file2... ”
	exit 1 # error for end
else
	arr=($(echo $1 | tr ',' ' '))
	echo $arr
	for i in "${arr[@]}"
	do
		if [[ ! -f $i ]]
		then
			echo "$i is not file"
		else
			echo -n "$(printf "%0$(wc -c <<< $i)d" "")" > $i
			rm $i
			echo "$i as been destroyed"
		fi
	done	
fi
