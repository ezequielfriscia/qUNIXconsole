#!/bin/bash
#qUNIXconsole (c) by Ezequiel L. Friscia>
#https://www.linkedin.com/in/ezequielfriscia/
#
#qUNIXconsole is licensed under a
#Creative Commons Attribution-ShareAlike 4.0 International License.
#
#You should have received a copy of the license along with this
#work. If not, see <http://creativecommons.org/licenses/by-sa/4.0/>.

#To set a default USB Serial Adapter in Option 1 modify the line:
#screen /dev/tty.usbserial-AC01PZ7M 9600
#
#Replace the command with the interface you will use. 
#To find it run in shell: ls -ltr /dev/*usb* 

clear

menu='
Select Desired Interface:
-------------------------

1. Predefined Cable
2. New USB Console Cable
3. Other(s)
4. Exit

Select Option ( 1 | 2 | 3 | 4 ): ' 

while true; do
	clear
	echo -n "$menu"
	read num
		if [ $num = 1 ]
			then
			screen /dev/tty.usbserial-AC01PZ7M 9600		#This is the line to modify
		elif [ $num = 2 ]
			then
			echo ""
			ls -ltr /dev/*usb*
			echo ""
			read -p 'Enter Interface Serial Number: ' serial
			screen /dev/tty.usbserial-$serial 9600
		elif [ $num = 3 ]
			then
			echo ""
			ls -ltr /dev/*usb*
			echo ""
			read -p 'Write Interface to Use (After /dev/): ' interface
			screen /dev/$interface 9600
		elif [ $num = 4 ]
			then
			clear
			break
		else
			echo ""
			echo 'Enter a valid option!'
			read -p "Press enter to continue"
		fi
done
