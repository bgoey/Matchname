# Matchname
Match name is  for loop which goes through the first three and last three letters of someones name. 
If there is a match it gives you the index on what name in x matches to what index in y.
By getting the index you can paste another column in y to your dataset in x without deleting any other names in x.


for(i in 1:257){
  temp = which((substr(x$names[i],1,3)==substr(y$names,1,3))&(substrRight(x$names[i], 3) == substrRight(y$names, 3)))
  if(length(temp) == 0){
    l[i] <- NA
  } else{
    l[i] = temp 
  } 
}

x$email=y$Email(l)

#extra info
Be sure to make a vairable l=NULL
Furthermore make sure the columnames within you x and y datasets are named names. 

