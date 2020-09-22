# Task 1
For this task I downloaded a csv file about Pokemon from Kaggle (The file can be found here https://www.kaggle.com/abcsds/pokemon)
I uploaded the file to one of my GitHub repositories
- I downloaded it in my linux terminal from there via the following command:
`wget https://raw.githubusercontent.com/myarmolinsky/CISC-3140/master/Pokemon.csv`
- I showed the first 10 lines of the csv via the following command:
`head -n 10 Pokemon.csv`
- I showed how many items there are in the csv via the following command:
`wc -l Pokemon.csv`
- I showed the third column of the csv via this command:
`awk -F "\"*,\"*" '{print $3}' Pokemon.csv`
The above line uses awk.  -F tells it to split the csv into columns by commas and the content in the curly braces tells it to print the third column
- I sorted the csv in alphabetical order based on the second column via this command:
`sort -t ',' -k2 -k1 <(tail -n+2 Pokemon.csv) -o Pokemon.csv`
The above line uses sort and overwrite Pokemon.csv with its output.  `(tail -n+2 Pokemon.csv)` make it so that we excldue the header line.
- I prove that I changed the order by calling this command again:
`head -n 10 Pokemon.csv`
- I prove that nothing got added or removed from the file by calling this command again:
`wc -l Pokemon.csv`
# Task 2
For this task I created a script file "myscript.sh", put the commands I used in the previous task into it, and executed it.
- I used the following command to create the mycript.sh file:
`touch myscript.sh`
- I used the following command to open the file with vim and write in it:
`vim myscript.sh`
Once I opened the file, I tapped the i key to begin inserting into file, entered all the commands I used in the previous task on separate lines, tapped the escape key, and typed :wq to save and quit the vim editor
- I used the following command to prepare the file for execution:
`chmod +x myscript.sh`
- I used the following command to execute the file:
`./myscript.sh`
# Task 3
