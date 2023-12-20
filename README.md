# LAB-2.1
66543206088-7 นายศุภกร ศิริเมืองมูล

#include <stdio.h>
#include <string.h>

void reverse( char str1[], char str2[] ) ;

int main() {
 	char text[ 50 ] = "I Love You" ;
 	char out[ 50 ] ;
 	
 	reverse( text, out ) ;
 
	printf( "Original : %s\n", text ) ;
	printf( "Reversed : %s\n", out ) ;
	
	return 0;
}//end function


void reverse( char str1[], char str2[] ) {

	int length = 0 ;
	int i, j = 0 ;
	strcpy( str2, str1 ) ;
	//calculates the length of the input string str1 by loop until it encounters the null terminator '\0'
	while ( str1[length] != '\0' ) {
		length++;
	} 
    //Swap characters to reverse the string
    //--------- < for revese, > for original --------------//
    for (i = 0, j = length - 1; i < j; i++, j--) {
        char hold = str2[i] ;
        str2[i] = str2[j] ;
        str2[j] = hold ;
    }//end for
}//end function
