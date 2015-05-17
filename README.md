# Repository-6
Create a class Rectangle with attributes length and width, each of which defaults to 1. Provide methods that calculate the rectangle’s perimeter and area. It has set and get methods for both length and width. The set methods should verify that length and width are each floating-point numbers larger than 0.0 and less than 20.0. Write a program to test class Rectangle.


public class Rectangle 
{
	private float Length;
	private float Width;
	private float Perimeter;
	private float Area;
	public float getLength()
	{
		return Length;
	}
	public void setLength(float L)
	{
		 if (L < 0.0 && L >= 20.0) 
		      {
		         throw new IllegalArgumentException(
		            "Length was out of range");
		      }

		      this.Length = L;
	} 
	
	public void setWidth(float W)
	{
		if (W < 0.0 || W >= 20.0) 
	      {
	         throw new IllegalArgumentException(
	            "Width was out of range");
	      }

	      this.Width = W;
	}
	public float getWidth()
	{
		return Width;
	}
	public float Perimeter(float L, float W)
	{
		
		if (L < 0.0 || L >= 20.0 ||W < 0.0 || W >= 20.0)
		{
			throw new IllegalArgumentException(
		            "Length and width was out of range");
		}
		else
		{
			Perimeter= 2*(L+W);
		}
		return Perimeter;
		
	}
	public float Area(float L, float W)
	{
		if (L < 0.0 || L >= 20.0 ||W < 0.0 || W >= 20.0)
		{
			throw new IllegalArgumentException(
		            "Length and width was out of range");
		}
		else
		{
			Area= L*W;
		}
		return Area;
	}
		
}
//Test Program
import java.util.Scanner;


public class RectangleTest 
{
	public static void main (String args[])
	{
		Scanner input=new Scanner (System.in);
		Rectangle rectangle= new Rectangle();
		System. out.print("Enter Length: ");
		float L=input.nextFloat();
		rectangle.setLength(L);
		System. out.print("Enter Width: ");
		float W=input.nextFloat();
		rectangle.setWidth(W);
		System.out.printf("Length of Rectangle is : %s\n",
				rectangle.getLength());
		System.out.printf("Width of Rectangle is : %s\n",
				rectangle.getWidth());
		System.out.printf("Perimeter is : %s\n",
				rectangle.Perimeter(L,W));
		System.out.printf("Area is : %s\n",
				rectangle.Area(L,W));	
	}
}
