# swash-gw-periodic

sedOlaFlow case setups for a gravel, 1:10 beach under monochromatic (MT3G) and irregular (IT3G) wave forcing. A description of the cases is included in (Delisle et al., in review, JGR: Oceans). 

### How to Simulate ###
1. foamCleanPolyMesh  
2. blockMesh  
3. snappyHexMesh -overwrite  
4. Go to 0 folder, make non-org files  
 cp -r alpha.water.org alpha.water    
5. setFields  
6. SedOlaFlow (can be run in parallel)

***To simulate a case with an elevated groundwater level:*** 
1. Copy desired slope file, either "slopeGW_hg01.stl" (h<sub>g</sub> = 0.1) or "slopeGW_hg02.stl" (h<sub<g</sub> = 0.2) into case folder 
2. Rename copied file to "slopeGW.stl"
3. Go to system folder, delete setFieldsDict file 
4. Rename setFieldsDict_gw to "setFieldsDict".
5. Follow simulation instructions in section above. 
