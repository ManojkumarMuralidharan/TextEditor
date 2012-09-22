TextEditor
==========

A basic implementation of text editor that allows to insert, delete and modify lines in the editor using a balanced binary tree.

This tree structure supports the following operations
	- text_t * create_text() creates an empty text, whose length is 0.
	
	- int length_text( text_t *txt) returns the number of lines of the current text.
	
	- char * get_line( text_t *txt, int index) gets the line of number index, if such a line exists, and  returns NULL else.

	- void append_line( text_t *txt, char * new_line) appends new line as new last line.

	- char * set_line( text_t *txt, int index, char * new_line) sets the line of number index, if such a line exists, to new line, and returns a pointer to the previous line of that number. If no line of that number exists, it does not change the structure and returns NULL.

	- void insert_line( text_t *txt, int index, char * new_line) inserts the line before the line of number index, if such a line exists, to new line, renumbering all lines after that line. If no such line exists, it appends new line as new last line.
	
	- char * delete_line( text_t *txt, int index) deletes the line of number index, renumbering all lines after that line, and returns a pointer to the deleted line.

The implementation is based on a balanced search tree, with the key mechanism impleted in such a way that we can easily increase the keys of all leaves above a certain key, without visiting more than O(log n) nodes. 

/* Reference 
insert, delete,left_rotation,right_rotation 
Advanced Data Structures
PETER BRASS
*/