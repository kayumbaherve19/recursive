# recursive
The given recursive method is as below.

public static double exponent(double a, int n)

{

return a * exponent(a,n-1);

}

Problem in given method:

The problem with this method is that it does not contain any base condition for stopping the recursion. This method will recursively call itself infinite times for every value of n which may create the problem of stack overflow exception in memory.

Solution:-

To fix the problem in the given method, we have to add a base condition for stopping the recursion. This stopping condition is as below.

We have to recursively call the exponent method only when the value of n is greater than 1 otherwise, we can simply return 1.
package recursion;

public class rec {
	 public static double exp(double a, int n)
	   {
	       // Checking condition for stopping the recursion
	if(n<=0)
	{
	return 1;
	}
	else
	{
	// recursive call to exponent function   
	return a * exp(a,n-1);
	}
	   }
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		double res = exp(2,4);
		System.out.println("The value of 2^4 is "+res);
	}

}
