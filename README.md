# Java
First we need to Read from a text file and save it in an array
Creat a method
Search for verbs and then print them out
for example for the output to be 
لعب: فعل ماضي etcc for all the words in the textfile


import java.io.*;
import java.util.*;
public class hello {
	static Scanner console = new Scanner (System.in);


	
	public static void main (String[] args) {
		
		String[] text = new String [500];
		
		try {
			
			BufferedReader reader = new BufferedReader(new FileReader("C:\\Users\\Lenovo\\Desktop\\DataFile.txt"));
			String line="";
			int counter =0;
			while (((line = reader.readLine()) !=null ) && (counter<500 )) {
				
				text[counter]=line;
				counter++;
			}
			for (String readline : text) {
				System.out.println(readline);
			}
			reader.close();
		}
		catch(Exception ex) {
				System.out.println("Exception: " + ex.getMessage());
				
			}
		
		}
			
		public static void verb(String[] arr) {
			String[] verb = new String[arr.length];
			
			for (int i=0; i<arr.length; i++) {
				char A = arr[i].charAt(0);
				char B = arr[i].charAt(0);
				char D = arr[i].charAt(0);
				char C = arr[i].charAt(arr.length-1);
			
				if ( A == 'ي' ) 
					System.out.println(arr[i] + "فعل مضارع");
			verb [i] = arr[i];
				 if (B =='ت')
					System.out.println(arr[i] + "فعل مضارع");
				verb [i] = arr[i];
				 if (D =='ا')
					System.out.println(arr[i] + "فعل امر");
				verb [i] = arr[i];
				 if (arr[i].length()-1==3)
					System.out.println(arr[i]+ "فعل ماضي");
					
				verb[i] = arr[i];
				
			} 
		
		
		
		
					 
				}
			
			
			}
		
