import java.util.Scanner;
class assign{
 public static void main( String...args) {
              
             // append();   // to append string + character replacing
            //  sw_use();   //use of switch
            //  sub_str();  
            //  sub_match();
            // str_rev();
             char_rev();
            }
       static public  void append()    // to append string + character replacing
                 {
                 System.out.println(" Enter first string");
                  Scanner obj = new Scanner(System.in);
                  String str1 = obj.nextLine();
                  // System.out.println(str1);
                  System.out.println(" Enter second string");
                  obj = new Scanner(System.in);
                  String str2 = obj.nextLine();
                  String str3= str1+' '+str2;
                  System.out.println(str3);

                  char arr[]= new char[str3.length()];    // replacement of character
            
                  System.out.println(" Enter character to replce (Remove)");
                  char ch = obj.next().charAt(0);
                  System.out.println(" Enter character to put");
                  char ch1 = obj.next().charAt(0);
                  for (int i=0 ;i< str3.length();i++)
                        if (ch==str3.charAt(i))
                             arr[i]=ch1;
                        else 
                          arr[i]=str3.charAt(i);
                        
                  System.out.println(arr);

                 }

      
 static public void sw_use()              //use of switch
                 {
                   char no;                              
               Scanner obj = new Scanner(System.in);
               System.out.println("Enter your grade in examination");
                no = obj.next().charAt(0);
                no = Character.toUpperCase(no);
               System.out.print("your grad is : -");
               System.out.println(no);
                switch(no) {
                             case 'A' :  System.out.println("You got 81 -100% marks in exam");
                                         break;
                             case 'B'  : System.out.println("You got 61 -80% marks in exam");  
                                          break;
                             case  'C'  : System.out.println("You got 51 -60% marks in exam");
                                          break;
                             case 'D'  : System.out.println("You got 41 -50% marks in exam");
                                          break;  
                               
                                        
                             default : System.out.println("not available");
                            }
                  }

   static public void sub_str()
                  {
                    System.out.println("Enter string");
                    Scanner obj= new Scanner(System.in);
                    String str= obj.nextLine();
                    System.out.println("enter start point");
                    int i=obj.nextInt();
                    System.out.println("enter end point");
                    int j =obj.nextInt();
                  //  System.out.print(str +' '+i+' '+j);

                    char arr[]= new char[str.length()];
                    for(int k=i-1; k<j;k++ )
                        arr[k]=str.charAt(k);
                    System.out.println(arr);

                  }


 static public void sub_match()
                  {
                    System.out.println("enter first string ");
                    Scanner obj = new Scanner(System.in);
                    String str1 = obj.nextLine();
                    System.out.println("second first string "); 
                    String str2 = obj.nextLine();
                    
                    char arr[] = new char[str1.length()];
                    char arr1[] = new char[str2.length()];
                    int k=0;
                    for(char c : str1.toCharArray())      // save in array 
                       {
                          arr[k]=c;
                           k++;
                        }
                     k=0;
                     for(char c : str2.toCharArray())
                       {
                          arr1[k]=c;
                           k++;
                        }                    
                   //  System.out.println(arr);
                  
                    for( int i =0; i<str1.length();i++)
                         for(int j=0; j<str2.length();j++)
                             if((i+j)<str1.length())
                             if(arr[i+j]==arr1[j])
                                if(j==(str2.length())-1)
                                  System.out.println("string found");
                     System.out.println(" string not found");    
                   }

public static void str_rev()
              {
                System.out.println(" Enter the string");
                 Scanner obj= new Scanner(System.in);
                 String str[] = obj.nextLine().split(" ");
                 for (int i=str.length -1; i>=0;i--)
                   System.out.print(" " +str[i]);
                   
                }
public static void char_rev()
              {
                System.out.println(" Enter the string");
                 Scanner obj= new Scanner(System.in);
                 String str = obj.nextLine();
                 char arr[]= new char[str.length()];
                 int k=0;
                 for(char c : str.toCharArray())      // save in array 
                       {
                          arr[k]=c;
                           k++;
                        }
                 for (int i=str.length() -1; i>=0;i--)
                   System.out.print(arr[i]);
                   
                }

           }
