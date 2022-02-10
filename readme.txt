******************************************************************************
**********************CSE522-Real Time Embedded Systems**********************
*****************************Assignment-3***************************************


Name - Raunak
ASU ID - 1217240245

Description : 

In this assignment, we have developed a thread tracing backend function, which logs the thread data, stores in a buffer and dumps the value on the screen, which is used to make vcd file for the analysis through gtkwave.



******************************************************************************
*******************Steps to compile and execute the code*********************



1. Copy the  RTES-Raunak_03.zip file in the zephyr/samples directory.

2. Unzip the RTES-Raunak_03.zip in the zephyr/samples directory.

3. apply the patch assignment3.patch to the zephyr source directory.

4. start the terminal go to zephyr folder and set the environment by the following commands,

	(i)   source zephyr-env.sh
	(ii)  export ZEPHYR_TOOLCHAIN_VARIANT=zephyr
	(iii) export ZEPHYR_SDK_INSTALL_DIR=Zephyr SDK installation directory
	
5. Go to zephyr/samples/trace_app folder

6. Create a folder named build using mkdir build command.

7. Go inside the folder build using cd build command.

8. Set the cmake environment using the following command,

	cmake -DBOARD=galileo ..
	
9. Then type the following command to make the binary,

	make
	
10. Now from the zephyr directory created inside build copy the zephyr.strip file to the kernel folder of SD card.

11. Now, assuming you sd card is prepared with bootia32.efi file and config file. Insert your sd card to the galileo board.

12. Now boot from SD card and load the zephyr kernel.

13. Now connect the ftdi cable and do chmod 777 tty/USB0.

14. start putty, set the logging to printable output and name the file as gtk.csv and set serial communication to 115200 and tty/USB0 and load.

15. Load the zephyr kernel, after a delay all the data will be dumped and stored in the gtk.csv file.

16. copy the gtk.csv file in the python(pycharm) project folder along with the python main file in the trace_app folder and execute the script to create the vcd file.

17. open the vcd file through gtkwave to observe the waveform.
	
	
*******************************************************************************
******************************Sample Output**********************************



Specified in the report.


