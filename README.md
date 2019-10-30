# Zip-List-of-Files-and-Folders-in-PHP
Zip a list of files and/or folders into an archive using a PHP function

* 	ZIP a list of files and folders
	-------------------------------
*
	Folders will be zipped recursively.
	If the destination zip file exists the file will be overwritten.
	Usage:
		Zip('$ziplist,'/path/to/compressed.zip',true);
	where $ziplist is a comma and space separated list of the form
		$ziplist = '../ItFigures, ../ItFigures.html, ../favicon.ico';
					^ a folder		^ a file			^ a file
	*
	*
	Third argrument sets zip structure:

	 IF third argrument to `true` files and subfolders will be added recursively under
	 each directory in $ziplist rather than in the zip folder root.
		ItFigures directory
		--- file 1
		--- file 2
		--- ItFigures subdirectory 1
		------ file 3
		------ file 4
		--- ItFigures subdirectory 2
		------ file 5
		------ file 6
		ItFigures.html file
		favicon.ico file

	IF the third argrument `false` or omitted, files and subfolders will be added
	recursively in the zip folder root:
		file 1
		file 2
		ItFigures subdirectory 1
		--- file 3
		--- file 4
		ItFigures subdirectory 2
		--- file 5
		--- file 6
		ItFigures.html file
		favicon.ico file
*
	Code modified from stackoverflow-dot-com/users/89771/alix-axel
	by Bob Wright, 10/2019
*/
