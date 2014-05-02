DICE-LAB---5---WEEK-11
======================
//  BY REINA OLARTE
// "DICE"  LAB #5  WEEK 11

public class Dice 
{
	static int COMPNumber;
	
	//  variables
	
	int ADDNumbers;
	
	int GENNumber;
	
	int NUMBbounces;
	
	int averageNumber;
	
	int i=1;
	
		public Dice()
		{

		}
		static int oneThrow()
		{
			int compNumber;
			
			COMPNumber = (1	 + (int)(Math.random() * 6));
			
			COMPNumber = COMPNumber;
			
			//System.out.printf("generated number: %d\n", compNumber);
			
			return COMPNumber;
			
		}
		public Dice(int bounces)
		{
			while(i <= bounces)
			{
				ADDNumbers += Throw();
				i++;
			}
			COMPNumber = ADDNumbers / bounces;		
		}
		public int Throw()
		{
			COMPNumber = (1	 + (int)(Math.random() * 6));
			

				return COMPNumber;
		}
		public int Throw(int bounces)
		{

			NUMBbounces = bounces;
			while(i <= bounces)
			{
				GENNumber = (1+(int)(Math.random() *6));
				
				System.out.printf("   The generated number is: %d\n", GENNumber);
				
				ADDNumbers += GENNumber;
				
				System.out.printf("   The Sum of the Number: %d\n", ADDNumbers);
				
				i++;
			}
			COMPNumber = ADDNumbers / NUMBbounces;
			
			return COMPNumber;
		}
		public int Throw(int dices, int bounces)
		{
			int totalNumber=0;
			
			int t;
			
			for(int x= 0; x<dices; x++)
				
			{
				System.out.printf("Throwing dice number %d\n ", x+1);
				
				t = Throw(bounces);
				
				totalNumber = totalNumber + t;
				
				System.out.printf(" The number generated for Dice %d is %d\n", x+1, totalNumber);
				
				COMPNumber += totalNumber;
			}
			return COMPNumber;
		}
		public int Value()
		{
			return COMPNumber;
		}
}

