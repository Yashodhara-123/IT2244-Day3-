# IT2244-Day3-
//Create and edit a TSV file
touch abc.tsv                      
vi abc.tsv 
# Create an empty file named abc.tsv 
# Open abc.tsv in the vi text editor for editing
                       
// File listing
ls -a
# List all files, including hidden ones                              

// Extract specific columns
cut -d$'\t' -f1 abc.tsv            
cut -d " " -f3 abc.tsv             
cut -d$'\t' -f1 abc.tsv            
cut -d ' ' -f1 abc.tsv             
cut -d ' ' -f2 abc.tsv             
#Extract the first column
#Extract the third column
#Another way to extract the first column
#Extract the first column
#Extract the second column

//Display file content
head -n2 abc.tsv                    
tail -n2 abc.tsv                   
head abc.tsv                       
head -8 abc.tsv                      
tail -8 abc.tsv                      
head -1 abc.tsv                      
tail -1 abc.tsv                     
head -n8 abc.tsv | tail -n1          
#Show the first 2 lines
#Show the last 2 lines
#Show the first 10 lines
#Show the first 8 lines
#Show the last 8 lines
#Show the first line
#Show the last line
#Show the 8th line

//Using awk for text processing
awk '{print}' abc.tsv               #### Print all lines 
awk '{print NF; exit}' abc.tsv       #### Print the number of fields in the first line
awk -F'\t' '{print NF; exit}' abc.tsv #### Print the number of fields using tab as a delimiter
awk '{print $3}' abc.tsv             #### Print the third column of each line

//Counting lines
wc -l abc.tsv                        #### Count and display the number of lines

//Filtering content with grep
head -n10 abc.tsv | grep 'dd'        #### Show first 10 lines and filter lines containing 'dd'
head -n7 abc.tsv | grep '56'         #### Show first 7 lines and filter lines containing '56'
