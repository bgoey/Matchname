# Matchname
Match two columns of names to each other by comparing the first three and the last three letters and than put the index of another column into a certain object.
Could for example be emails.


#start with creating l which is the length of the documents you wish to match
l=1:257

Matchonletters=function(x[z],y){
for(i in 1:257){
  temp = which((substr(x$names[i],1,3)==substr(y$names,1,3))&(substrRight(x$names[i], 3) == substrRight(y$names, 3)))
  if(length(temp) == 0){
    l[i] <- NA
  } else{
    l[i] = temp 
  } 
}
}
x$email=y$Email(l)


# be sure to select the right column in substr(x[i,1},1,3) the column name now is names
# the code needs some readjustment as to whether you 

