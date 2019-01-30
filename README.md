# IGLOSS
IGLOSS: iterative gapless local similarity search

Program takes four arguments:    proteome_file_name      query_file_name     scale     number_of_iterations

Proteome file can be in fasta or text format. 

Query file consists of one or more rows of amino acids symbols ARNDCQEGHILKMFPSTWYV. 
Symbols 'X' and 'x' standing for any amino acid symbol is allowed.  
One extra row of 0 and 1 is allowed, where 1 stands for a conserved position. 
All rows in the query file must be of equal length.  

Scale is a positive float. This parameter measures similarity between input query and the response. 
The higher it is - higher is the similarity.  

Number of iterations is selfexplanitory.

IGLOSS.cpp calls logistic.py to make a logistic fit of the data.

IGLOSSnopy.cpp is IGLOSS.cpp without calling logistic.py for logistic fit. 
It makes an estimation of logistic fit via mean and standard deviation.  


