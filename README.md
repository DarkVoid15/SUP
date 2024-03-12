import java.util.*;

public class AnagramExample {

public static void main(String[] args) {
Scanner input = new Scanner(System.in);

System.out.println("Enter first String value: ");
String str1 = input.nextLine();

System.out.println("Enter second String value: ");
String str2 = input.nextLine();

// Check if the two strings are of equal length
if (str1.length() != str2.length()) {
System.out.println("The two strings are not anagrams");
return;
}

// Convert the two strings to character arrays
char[] charArray1 = str1.toCharArray();
char[] charArray2 = str2.toCharArray();

// Sort the two character arrays
Arrays.sort(charArray1);
Arrays.sort(charArray2);

// Compare the two sorted character arrays
boolean isAnagram = Arrays.equals(charArray1, charArray2);

// Print the result
if (isAnagram) {
System.out.println("The two strings are anagrams");
} else {
System.out.println("The two strings are not anagrams");
}
}
}
