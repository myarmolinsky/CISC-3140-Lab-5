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
For this task I used my local unix ssh instead of the school's terminals.  I cloned a repository from my github onto which I put images for the sake of this lab (the repository can be found here: https://github.com/myarmolinsky/CISC-3140).  I used imagemagick to display an image, take an image, negate it's color, flip it horizontally, flip it virtically, and display it once all the changes have been made to it.  To do so, I made a script file called myscript.sh and gave it the following text:
```
display image1.jpg
convert -negate image1.jpg image1.jpg
convert -flop image1.jpg image1.jpg
convert -flip image1.jpg image1.jpg
display image1.jpg
```
The first line made the original image display.  The second line negated the image and replaced the original with the new one.  The third line flipped the new image horizontally and replaced it with the new one.  The fourth line flipped the new image vertically and replaced it with the new one.  Finally, the last line displays the new image after all the conversions.  Once I had the script made, I prepared it for execution using the `chmod +x myscript.sh` command and executed it via the `./myscript.sh` command.
