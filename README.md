ShellScriptSample
=================
###Running a shell script.
In order to run the shell script , in the terminal 
1) Go to the directory where the script is.
2) Give execute permission to the script you have created.
	
		sudo chmod 777 <script_name>

4) To execute the script 
		
		./<script_name>

###Here is a sample script.

		#!/bin/bash
		# My First Script
		declare -a filename=(hello.txt hello.doc)
		for i in ${filename[@]}
		do
			value=`cat $i`
			echo "$value"
		done

This script reads two different files `hello.txt` `hello.doc` and prints the content of the file one by one. 
We have saved the file names in the array `filename` .
The command `value=cat $i` reads the content of the file.
