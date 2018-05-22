# This is a make file written by Zhiyang Ong to create pictures in
# PDF format from MetaPost

# =============================================================

# Definition of macro flags...
# IMPORTANT NOTE: Makefile is written for Mac OS X 10.5.6

# Programs to generate pictures in PDF format from MetaPost source files
MP=				mpost
MPTOPDF=		mptopdf

# Types of files
SOURCE=			*.mp
# Picture files
PDF=			*.pdf
# Other file types
ONE=			*.1
LOG=			*.log
KEEP=			*.keep
TEMP=			*temp*
MPX=			*.mpx
FLS=			*.fls
# Temporary files generated from mpost compilation errors
TEMPFILES:=		mptextmp.mp mpxerr.tex mpgraph.mp


# UNIX commands/utilities that are used
RM=				rm -rf
TCH=			touch
OPEN=			open
ECHO=			@echo
TIME=			time -p #-lp
DATE=			date

# MetaPost source files used for generating pictures

# Names used to arrays of MetaPost files
# FILESNY FILESOR FILESSF FILESSV FILESLA FILESBC FILESHW FILESLB FILESELA FILESCOMPTON FILESPAS FILESSFV FILESW FILESV FILESTU FILESS FILESPR FILESNO FILESM FILESIL FILESH FILESG FILESDF FILESC FILESB FILESA
FILESALL		:= FILESNY FILESOR FILESSF FILESSV FILESLA FILESBC FILESHW FILESLB FILESELA FILESCOMPTON FILESPAS FILESSFV FILESW FILESV FILESTU FILESS FILESPR FILESNO FILESM FILESIL FILESH FILESG FILESDF FILESC FILESB FILESA


# Places in Greater Los Angeles - sorted in alphabetical order
FILESA			:= agoura_hills.mp alamitos_heights.mp alhambra.mp anaheim.mp arcadia.mp arlington_park.mp arroyo_seco.mp artesia.mp altadena.mp avalon_boulevard.mp
FILESB			:= baldwin_hills.mp beach_cities.mp bel_air.mp belmont_heights.mp beverly_hills.mp brentwood.mp buena_park.mp bunker_hill.mp burbank.mp
FILESC			:= calabasas.mp centinela_avenue.mp cerritos.mp chatsworth.mp chino_hills.mp claremont.mp compton.mp crenshaw.mp culver_city.mp cypress_park.mp
FILESDF			:= disneyland.mp dodger_stadium.mp eagle_rock.mp east_los_angeles.mp el_segundo.mp exposition_park.mp fairfax_avenue.mp fashion_district.mp figueroa_street.mp florence.mp
FILESG			:= gardena.mp glendale.mp granada_hills.mp griffith_park.mp
FILESH			:= hancock_park.mp hawthorne_boulevard.mp hermosa_beach.mp highland_avenue.mp highland_park.mp hollywood.mp huntington_park.mp huntington_beach.mp hyde_park.mp
FILESIL			:= imperial_highway.mp inglewood.mp inland_empire.mp jefferson_boulevard.mp jefferson_park.mp la_brea_avenue.mp la_cienega_boulevard.mp laguna_beach.mp long_beach.mp lynwood.mp
FILESM			:= macarthur_park.mp malibu.mp manhattan_beach.mp marina_del_rey.mp martin_luther_king_jr_boulevard.mp mayflower_village.mp melrose_hill.mp miracle_mile.mp monterey_hills.mp monterey_park.mp
FILESNO			:= newport_beach.mp north_hollywood.mp northridge.mp olympic_boulevard.mp ontario.mp
FILESPR			:= pacific_palisades.mp palisades.mp palos_verdes.mp pasadena.mp pico_boulevard.mp pomona.mp rancho_cucamonga.mp redondo_beach.mp
FILESS			:= san_bernardino.mp san_clemente.mp san_fernando.mp san_gabriel.mp san_marino.mp san_pedro.mp santa_clarita.mp santa_monica.mp sawtelle_boulevard.mp sepulveda_boulevard.mp sherman_oaks.mp sierra_madre_boulevard.mp simi_valley.mp six_flags_magic_mountain.mp skid_row.mp slauson_avenue.mp south_pasadena.mp sunset_boulevard.mp
FILESTU			:= thousand_oaks.mp torrance.mp universal_city.mp university_park.mp universal_studios_hollywood.mp
FILESV			:= van_nuys.mp venice_beach.mp venice_boulevard.mp ventura.mp vermont_avenue.mp vermont_park.mp vernon.mp
FILESW			:= walnut_park.mp washington_boulevard.mp watts.mp west_adams.mp west_alameda.mp west_covina.mp west_hollywood.mp west_los_angeles.mp western_avenue.mp westside_village.mp westwood.mp wilshire_boulevard.mp


# Places in Greater Los Angeles - sorted by location
FILESSFV			:= agoura_hills.mp burbank.mp dodger_stadium.mp granada_hills.mp griffith_park.mp malibu.mp northridge.mp san_fernando.mp simi_valley.mp six_flags_magic_mountain.mp santa_clarita.mp sherman_oaks.mp thousand_oaks.mp van_nuys.mp ventura.mp
FILESPAS			:= alhambra.mp arcadia.mp arroyo_seco.mp eagle_rock.mp glendale.mp highland_park.mp monterey_hills.mp monterey_park.mp pasadena.mp san_gabriel.mp san_marino.mp sierra_madre_boulevard.mp south_pasadena.mp west_covina.mp
FILESCOMPTON		:= artesia.mp avalon_boulevard.mp compton.mp crenshaw.mp gardena.mp hawthorne_boulevard.mp lynwood.mp watts.mp
FILESELA			:= chino_hills.mp claremont.mp east_los_angeles.mp east_los_angeles.mp huntington_park.mp ontario.mp pomona.mp rancho_cucamonga.mp san_bernardino.mp vernon.mp walnut_park.mp
FILESLB			:= anaheim.mp cerritos.mp cypress_park.mp disneyland.mp imperial_highway.mpx laguna_beach.mp long_beach.mp newport_beach.mp san_clemente.mp san_pedro.mp
FILESHW			:= beverly_hills.mp brentwood.mp centinela_avenue.mp hancock_park.mp highland_avenue.mp hollywood.mp la_brea_avenue.mp la_cienega_boulevard.mp marina_del_rey.mp miracle_mile.mp north_hollywood.mp olympic_boulevard.mp pacific_palisades.mp pico_boulevard.mp santa_monica.mp sawtelle_boulevard.mp sepulveda_boulevard.mp sunset_boulevard.mp universal_city.mp universal_studios_hollywood.mp venice_beach.mp venice_boulevard.mp west_hollywood.mp west_los_angeles.mp westwood.mp wilshire_boulevard.mp
FILESBC			:= beach_cities.mp el_segundo.mp hermosa_beach.mp huntington_beach.mp manhattan_beach.mp palos_verdes.mp redondo_beach.mp torrance.mp
FILESLA			:= culver_city.mp exposition_park.mp fairfax_avenue.mp fashion_district.mp figueroa_street.mp inglewood.mp jefferson_boulevard.mp jefferson_park.mp macarthur_park.mp martin_luther_king_jr_boulevard.mp skid_row.mp university_park.mp vermont_avenue.mp vermont_park.mp washington_boulevard.mp west_adams.mp western_avenue.mp slauson_avenue.mp
 


# Places in the Silicon Valley
FILESSV			:= agnews_village.mp alameda.mp cupertino.mp fremont.mp los_gatos.mp milpitas.mp mountain_view.mp palo_alto.mp redwood_city.mp san_jose.mp santa_clara.mp santa_cruz.mp silicon_valley.mp stanford.mp sunnyvale.mp

# Places in the Bay Area
FILESSF			:= alameda.mp berkeley.mp fremont.mp golden_gate_bridge.mp oakland.mp richmond.mp san_francisco.mp

# Places in Portland, Oregon
FILESOR			:= beaverton.mp bridgetown.mp columbia_river.mp concordia.mp hawthorne_bridge.mp hillsboro.mp lake_oswego.mp niketown.mp oregon.mp oswego_lake.mp pdx.mp portland.mp rip_city.mp silicon_forest.mp southwest_hills.mp stumptown.mp the_city_of_roses.mp the_grotto.mp willamette_river.mp

# Places in New York City, New York
FILESNY			:= bedford.mp bedford-stuyvesant.mp big_apple.mp brighton_beach.mp broadway.mp brooklyn.mp brooklyn_heights.mp central_park.mp coney_island.mp downtown_manhattan.mp greenwich_village.mp harlem.mp hudson_river.mp italian_harlem.mp jackson_heights.mp lenox_hill.mp long_island.mp lower_east_side.mp lower_manhattan.mp madison_square.mp manhattan.mp manhattan_beach.mp new_york_city.mp ocean_parkway.mp rucker_park.mp queens.mp soho.mp spanish_harlem.mp staten_island.mp stuyvesant_heights.mp the_bronx.mp times_square.mp union_square.mp upper_east_side.mp upper_west_side.mp wall_street.mp west_village.mp yorkville.mp




#alicia.mp borkum.mp cerritos.mp


















# Files that work
WORKINGFILES	:= agnews_village.mp agoura_hills.mp alameda.mp alhambra.mp beaverton.mp bedford-stuyvesant.mp bedford.mp berkeley.mp big_apple.mp bridgetown.mp brighton_beach.mp broadway.mp brooklyn.mp brooklyn_heights.mp columbia_river.mp concordia.mp coney_island.mp cupertino.mp downtown_manhattan.mp eagle_rock.mp fremont.mp harlem.mp hudson_river.mp italian_harlem.mp jackson_heights.mp lenox_hill.mp long_island.mp los_gatos.mp lower_east_side.mp madison_square.mp manhattan_beach.mp milpitas.mp mountain_view.mp new_york_city.mp northridge.mp oakland.mp ocean_parkway.mp oregon.mp palo_alto.mp pdx.mp portland.mp redwood_city.mp richmond.mp rip_city.mp san_fernando.mp san_jose.mp	 santa_clara.mp santa_clarita.mp santa_cruz.mp sherman_oaks.mp silicon_valley.mp simi_valley.mp southwest_hills.mp spanish_harlem.mp stanford.mp staten_island.mp stumptown.mp sunnyvale.mp the_bronx.mp union_square.mp upper_east_side.mp wall_street.mp west_village.mp yorkville.mp














########################################################################
########################################################################
########################################################################

# Options to compile MetaPost source files with:

# Compiles MetaPost source file without having to interact with the user
# by entering the interactive mode, which the user can escape from by
# entering "S"
#-file-line-error

# For the MetaPost source file [filename].mp, it creates a file named:
# [filename].fls
#-recorder


# Use this command:
# mpost -recorder -file-line-error 

########################################################################
########################################################################
########################################################################














# =============================================================

# Definition of Target Rules


# TO BE UPDATED
########################################################################
# Compile the MetaPost source files into PDF...
# Use a FOR loop to sweep through the list of MetaPost source files?
# 
all:
	@echo ===Run MetaPost on the MetaPost source files...
	for i1 in $(WORKINGFILES); do\
		$(MP) $$i1; \
	done
	
	@echo ===Run MPtoPDF on the MetaPost source files...
	for i1 in $(WORKINGFILES); do\
		$(MPTOPDF) $$i1; \
	done

	









########################################################################
# Run MetaPost on MetaPost source files
metapost:
	@echo ===Run MetaPost on MetaPost source files in the list FILESSV ...
	for i1 in $(FILESSV); do\
		$(MP) $$i1; \
	done








########################################################################
# Open pictures files in PDF format
pdf:
	@echo ===Open pictures files in PDF format ...
	$(OPEN) $(PDF)








########################################################################
# Run mptopdf on MetaPost processed files
mptopdf:
	@echo ===Run mptopdf on MetaPost processed files in the list FILESSV ...
	for i1 in $(FILESSV); do\
		$(MPTOPDF) $$i1; \
	done





########################################################################
# Create file(s) for use, test, and experimentation
create:
	@echo ===Creating a list of files from the list FILESSV ...
	for i1 in $(FILESSV); do\
		$(TCH) $$i1; \
	done








########################################################################
# Create file(s) for use, test, and experimentation
create1:
	@echo ===Creating a list of files from the list FILESOR ...
	for i1 in $(FILESOR); do\
		$(TCH) $$i1; \
	done	




########################################################################
# Create file(s) for use, test, and experimentation
create2:
	@echo ===Creating a list of files from the list FILESSF ...
	for i1 in $(FILESSF); do\
		$(TCH) $$i1; \
	done	







########################################################################
# Create file(s) for use, test, and experimentation
create3:
	@echo ===Creating a list of files from the list FILESNY ...
	for i1 in $(FILESNY); do\
		$(TCH) $$i1; \
	done






########################################################################
# Create file(s) for use, test, and experimentation
create4:
	@echo ===Creating a list of files from the list FILESSFV ...
	for i1 in $(FILESSFV); do\
		$(TCH) $$i1; \
	done










########################################################################
# Create file(s) for use, test, and experimentation
create5:
	@echo ===Creating a list of files from the list FILESPAS ...
	for i1 in $(FILESPAS); do\
		$(TCH) $$i1; \
	done














########################################################################
# Remove all the output file(s)
clean:
	@echo ===Removing *.1 files from the directory...
	$(RM)	$(ONE)
	@echo ===Removing *.log files from the directory...
	$(RM)	$(LOG)
	@echo ===Removing *.keep files from the directory...
	$(RM)	$(KEEP)
	@echo ===Removing *temp* files from the directory...
	$(RM)	$(TEMP)
	@echo ===Removing *.mpx files from the directory...
	$(RM)	$(MPX)
	@echo ===Removing *.fls files from the directory...
	$(RM)	$(FLS)
	@echo ===Removing temporary files generated by: mpost
	for i1 in $(TEMPFILES); do\
		$(RM) $$i1; \
	done






########################################################################
# Remove all the PDF file(s)
cleanpdf:
	@echo ===Removing *.pdf files from the directory...
	$(RM)	$(PDF)






	
	
	
	
	
########################################################################
# Count the number of lines in my source files
# cat *.mp | wc -l
numlines:
	@echo == Count the number of lines in my source files
	cat	$(SOURCE) | wc -l
	
		
			














# TO BE UPDATED
########################################################################
# The options for make targets are:
help:
	@echo The options are...
	@echo all________Compile all source files and link their
	@echo ___________object code, and run the program
	@echo clean______Remove all executables, object files,
	@echo ___________and output files
	@echo run________Execute the program
	@echo numlines___Count the number of lines in the source
	@echo ___________code and header files
