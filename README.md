# binding-site-analysis
Codes to analyze VASP CONTCAR files to identify and classify adsorption binding sites

#COMPILE VASP ADSOPRTION DATA
#INPUT: VASP CONTCAR DATA, PARAMETER .txt FILE, OSZICAR OPTIONAL
#EVAN KERIN - EDIT 1.26.2022
#PYTHON 3.9.7
#DEPENDENCIES: ase , ase.io , os , openpyxl , math 


INPUT:

	1) COMPILEPARAM.txt file with keyword written on independent lines

		KEYWORDS:
			
		ATOPMIN_## 	-	Min atop binding threshold in A
		ATOPMAX_## 	-	Max atop binding threshold in A
		BRIDGEDMIN_##	-	Min bridged binding threshold in A
		BRIDGEDMAX_##	-	Max bridged binding threshold in A
		MAXDIST_##	-	Max atom-atom distance script will compare
		ATOM_##_## 	-	Declaring Adsorbate-Adsorbent Combinations
		OSZICAR=####	-	True/False for if OSZICAR of same name as CONTCAR included

			EX: ATOM_S_Cu

		
	2) UNIQUEFILENAME.CONTCAR VASP Files in folder

OUTPUT:

	1) DataResults.xlsx with "Data_Overview" sheet ordering selected adsorbate - adsorbent pairs with their closest distances and classification. 
