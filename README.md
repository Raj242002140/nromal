# nromal
teachar work
import java.util.Scanner;

class Main
{
	public static void main(String[] args)
	{
		Scanner in=new Scanner(System.in);
		int number;
		System.out.print("Enter number: ");
		number=in.nextInt();

		All od=new All();
        int no;
        // do
        // {
        System.out.print("Enter no: ");
        no=in.nextInt();
        if(no==1)
        {
		int sum=od.add(number);
		System.out.println("Sum:"+sum);
        }
        else if(no==2)
        {
		int fact=od.fact(number);
		System.out.println("Fact:"+fact);
        }
        else if(no==3)
        {
		od.perfect(number);
    }
        else if(no==4)
        {
		All.strong(number);
        }
    }
    // while(no<5);
    // }
	}
class All
{
	public static int add(int n)
	{
		if(n==0)
		{
			return 0;
		}
		int sum=n+add(n-1);
		return sum;
	}

	public static int fact(int n)
	{
		if(n==0 ||n==1)
		{
			return 1;
		}
		int pro=n*fact(n-1);
		return pro;
	}

	public static void perfect(int n)
	{
		int sum=0;
		for(int i=1; i<n; i++)
		{
			if(n%i==0) {
				sum=sum+i;
			}
		}
		if(n==sum)
		{
			System.out.println("perfect number:"+n);
		}
		else
		{
			System.out.println(" no perfect number: "+n);
		}
	}

	public static void strong(int n)
	{
		int sum=0,g=n;
		while(n!=0)
		{
			int n1=n%10;
			int c=1;
			while(n1!=0)
			{
				c=c*n1;
				n1--;
			}
			sum=sum+c;
			n=n/10;
		}
		if(g==sum)
		{
			System.out.println("Strong number"+g);
		}
		else
		{
			System.out.println(" no Strong number: "+g);
		}
	}
}
