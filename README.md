#FUNCTION PatEx(Type , Num_Locations, Num_Components, Elements_List, Locations, Components, CID, File_Name, Entity_Sort, Value_Sort, Sort_Type)

#----------Stress_Frame function Parameters

PatEx(A,B,C,D,E,F,G,H) Parameters

A) Type. Report Type Keywords

GF : Grid Point Forces
GM : Grid Point Moments
SS_Z1 : Shell Stresses at Z1
SS_Z2 : Shell Stresses at Z2
BarF : Bar Forces
BeamF : Beam Forces
SF : Shell Forces

B) Number of needed location components. i.e if X, Y locations needed write 2. If it is zero, Locations parameter (D) will be ignored. 

B) Number of needed stress or force components. i.e if X, Y, Z comps needed parameter is 3, if only X is needed it is 1

C) Element Numbers.

D) Which Location components needed, as an array. i.e ["YLOC","ZLOC",""] to derive Y and Z locations. 

E) Needed Force/Stress components. IT can be XX, YY, ZZ for principal and XY, YZ, XZ shear components. Sample imput ["XX","YY","ZZ"]

F) Coordinate Sytem ID. Attention: CID Has to be in the model otherwise it will not produce the results

G) File Name. Name of the file. States how will the result file is being called when it is being created. 

H) Can be "LoadCase" or "Entity". Will the result be Loadcase based or Entity based. 

I) Column Number for Sorting. The result data will be sorted according to this column. 

J) The results will be in Ascending or Descending order. 


#---------



#---------
Freebody function paramters. 

#Attention: The script deletes the freebody.dat file (if it exists) before starting to produce output. 

#FUNCTION PatEx_Freebody(Sum_Point, Chosen_Ones, FB_CID, FB_File_Name)

PatEx_Freebody(A,B,C,D)
A) Summation Point, can be a node or a virtual point
B) Selected Nodes and Elements
C) Coordinate System to transfer the loads
D) Output File Name
