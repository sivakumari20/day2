# day2

package First_one;
import java.util.Scanner;
import java.lang.Math;

public class armstrongnumber {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc =new Scanner(System.in);
		System.out.println("enter a number");
		int x=sc.nextInt();
		int y=0,count=0;
		int temp=x;
		while(temp>0)
		{
		  temp=temp/10;
			  count+=1;
		  }
		temp=x;
		int sum=0;
		while(temp>0)
		{
			y=temp%10;
			sum=(int) (sum+Math.pow(y,count));
			temp=temp/10;
			
		}
		if (sum==x)
		{
         System.out.println("armstrong number");
	}
		else
		{
			System.out.println("not a armstrong number");
		}
**** gcd of a number****
}}
package First_one;
import java.util.Scanner;
import java.lang.Math;

public class armstrongnumber {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc =new Scanner(System.in);
		System.out.println("enter a number");
		int x=sc.nextInt();
		System.out.println("enter a number");
		int y=sc.nextInt();
		
		int gcd=findgcd(x,y);
		System.out.println(gcd);
	}

    public static int findgcd(int a,int b) {
			if (b>a)
			{
				int temp=a;
				a=b;
				b=temp;
			}
			while(b!=0)
				
			{
				int temp=b;
				b=a%b;
				a=temp;
			}
		return a;
		}
}

*** binary to decimal**
package First_one;

import java.util.Scanner;

public class decimaltobinary {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc =new Scanner(System.in);
		System.out.println("enter a number");
		int x=sc.nextInt();
		int i=0;
		int[] elements=new int[13];
		while(x>0)
		{
			elements[i++]=x%2;
			x=x/2;
		}
		System.out.println("binary number of a given decimal number is");
		for(int j=i-1;j>=0;j--)
		{
			
			System.out.print(elements[j]);
		}
	}

}
***matrix multiplication**
import java.util.Scanner;

public class matrixmultiplication {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc =new Scanner(System.in);
		System.out.println("enter a number");
		int x=sc.nextInt();//no of rows of 1
		System.out.println("enter a number");
		int y=sc.nextInt();//no of colomns of 1
		System.out.println("enter a number");
		int a=sc.nextInt();//no of rows of 2
		System.out.println("enter a number");
		int b=sc.nextInt();//no of colomns of 2
		int[][] matrix1=new int [x][y];
		int[][] matrix2=new int [a][b];
		int[][] matrix3=new int [x][b];
		int i =0;int j=0;
		
		if (y!=a) {
			System.out.println("matrix multiplication is not possible");
		}
		System.out.println("enetr elements of first matrix");
		for (i=0;i<x;i++)
			{
				for ( j=0;j<y;j++)
				{
					 matrix1[i][j]=sc.nextInt();
				}
			}
		System.out.println("enetr elements of first matrix");
		for (i=0;i<a;i++)
			{
				for ( j=0;j<b;j++)
				{
					 matrix2[i][j]=sc.nextInt();
				}
			}
		for (i=0;i<x;i++)
			{
				for ( j=0;j<b;j++)
				
					 {
					 matrix3[i][j]=0;
					 for ( int k=0;k<y;k++)
					 {
					 matrix3[i][j]+=matrix1[i][k]*matrix2[k][j];				}
			}
			}
				for (i=0;i<x;i++)
				{
					for ( j=0;j<b;j++)
					{
		System.out.print(matrix3[i][j]);
		
	}
System.out.println();
}
}
}
***finding duplicate numbers***
package First_one;

import java.util.Scanner;

public class duplicate {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc =new Scanner(System.in);
		System.out.println("enter a number");
		int x=sc.nextInt();
		int[] arr=new int[x];
		System.out.println("enter array alements");
		
		for (int i=0;i<x;i++)
		{
			int y=sc.nextInt();
			arr[i]=y;
					
		}
		findAndPrintDuplicates(arr);
    }

    public static void findAndPrintDuplicates(int[] arr) {
        System.out.println("Duplicate Elements:");
        for (int i = 0; i < arr.length; i++) {
            for (int j = i + 1; j < arr.length; j++) {
                if (arr[i] == arr[j]) {
                    System.out.print(arr[i] + " ");
                    break; // To avoid printing the same duplicate multiple times
                }
            }
        }
	}

}
***duplicate using hashmap***

package First_one;
import java.util.Scanner;
import java.util.HashSet;
public class duplicageusinghash {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc =new Scanner(System.in);
		System.out.println("enter a number");
		int x=sc.nextInt();
		int[] arr=new int[x];
		System.out.println("enter array alements");
		
		for (int i=0;i<x;i++)
		{
			int y=sc.nextInt();
			arr[i]=y;
					
		}
		findAndPrintDuplicates(arr);
    }
	 public static void findAndPrintDuplicates(int[] arr)
	 {
		 HashSet<Integer> uniqueelements =new  HashSet<>();
		 HashSet<Integer> duplicateelements =new  HashSet<>();
		 for(int element :arr)
		 {
			 if(!uniqueelements.add(element))
			 {
				 duplicateelements.add(element);
			 }
		 
	        }
		 for(int duplicate:duplicateelements)
		 {
			 System.out.println(duplicate);
		 }
	    }

	}
***binarysearch***
package First_one;

import java.util.Scanner;
import java.util.Arrays;

public class binartsearch {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc =new Scanner(System.in);
		System.out.println("enter a number");
		int x=sc.nextInt();
		int[] arr=new int[x];
		System.out.println("enter array alements");
		
		for (int i=0;i<x;i++)
		{
			int y=sc.nextInt();
			arr[i]=y;
					
		}
		System.out.println("enter the element you want to search");
		int key=sc.nextInt();
		 Arrays.sort(arr);
		 int a=binarysearch(arr,0,arr.length-1,key);
		 System.out.println(a);

	}
	public static  int binarysearch(int[] arr,int first,int last,int key)
	{
		
		while(first<=last)
		{
			int mid=(first+last)/2;
			if (arr[mid]<key)
			{
				first=mid+1;
			}
			else if(arr[mid]>key)
			{
				last=mid-1;
			}
			else
			{
				return mid;
			}
		}
		return -1;
	}

}
***wordfrequency***
package First_one;

//import java.util.Scanner;
import java.util.HashMap;

public class wordfrequency {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		//Scanner sc =new Scanner(System.in);
	//	System.out.println("enter a string");
		//String x=sc.next();
		String x="hey bro how are you are";
		HashMap <String,Integer> map=new HashMap<>();
		String arr1[]=x.split(" ");
		for(String word :arr1)
		{
			if(map.containsKey(word))
			{
				//int count=map.get((word)+1);
				map.put(word,map.get(word)+1);
			}
			else
			{
				map.put(word,1);
			}
		}
                System.out.println(map);
            }
        
		
	}
***finding the missing number***
package First_one;

import java.util.Scanner;
import java.util.Arrays;

public class missingnumber {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc =new Scanner(System.in);
		System.out.println("enter a number");
		int x=sc.nextInt();
		int [] arr=new int[x];
		int i=0;
		for ( i=0;i<x;i++)
		{
			int y=sc.nextInt();
			arr[i]=y;
		}
		Arrays.sort(arr);
		int n=arr.length+1;
		int sum=n*(n+1)/2;
		int sum1=0;
		
		for ( i=0;i<x;i++)
		{
			sum1=sum1+arr[i];
		}
		int diff=sum-sum1;
		System.out.println(diff);
	}

}

***finding the triplets***

package First_one;
import java.util.Scanner;
import java.lang.Math;

public class alltriplets {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc=new Scanner(System.in);
		System.out.println("enter the number");
		int x=sc.nextInt();
		triplets(x);
		

	}
	public static void triplets(int limit)
	{
		for (int a=1;a<=limit;a++)
		{
			for(int b=a+1;b<=limit;b++)
			{
				int csquare=a*a+b*b;
				int c=(int)Math.sqrt(csquare);
				if(c*c==csquare&& c<=limit)
				{
					System.out.println( a+ " ," + b +", " + c );
				}
			}
		}
	}

}

