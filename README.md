FUNCTION PatEx(Type , Num_Locations, Num_Components, Elements_List, Locations, Components, CID, File_Name, Entity_Sort, Value_Sort, Sort_Type)

#----------PatEx function Parameters

PatEx(A,B1,B2,C,D,E,F,G,H) Parameters

A)
GF : Grid Point Forces
GM : Grid Point Moments
SS : Shell Stress
BF : Bar Force

B1) Number of needed location components. i.e if eg X, Y locations needed write 2
	CAUTION:	this input is directly related to parameter D !
				choosing "0" (zero) will neglect the parameter D

B2) Number of needed stress or force components. i.e if X, Y, Z comps needed parameter is 3, if only X is needed it is 1
	CAUTION:	this input is directly related to parameter E !
				choosing "0" (zero) will neglect the parameter Element
				
C) Element IDs.

D) Which Location components needed, as an array.
	Sample input: ["YLOC","ZLOC",""] to derive Y and Z locations. => then B1 MUST be: 2
	CAUTION: do NOT set eg ["","","ZZ"] since patran searches for the 1 component and it is empty!

E) Needed Force/Stress components. IT can be XX, YY, ZZ for principal and XY, YZ, XZ shear components. 
	Sample imput: ["XX","YY","ZZ"] => then B2 MUST be: 3
	CAUTION: do NOT set eg ["","","ZZ"] since patran searches for the 1 component and it is empty!
	
F) CID. Attention: CID Has to be in the model otherwise it will not produce the results

G) File Name. Name of the file. States how will the result file is being called when it is being created. 

H) Can be "LoadCase" or "Entity". Will the result be Loadcase based or Entity based. 

I) Column Number for Sorting. The result data will be sorted according to this column. 

J) The results will be in Ascending or Descending order. 


#---------

Recommended: before Running clean the output directory from plain text files. 


#---------

PatEx_Freebody(A,B,C,D)
A) Summation Point, can be a node or a virtual point
B) Selected Nodes and Elements
C) Coordinate System to transfer the loads
D) Output File Name
