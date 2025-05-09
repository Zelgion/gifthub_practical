# gifthub_practical
using System;
class Car
{
    	public int Speed         {get; private set;}
        public double Mileage    {get; private set;}
        public double FuelLevel  {get; private set;}
        public string Make       {get; private set;}
        public string Model      {get; private set;}
        
        
        public Car (string make, string model)
        {
        Make      = make;
                Model     = model;
                Speed     = 0;
                Mileage   = 0;
        }
        
        public void StartEngine()
        {
        Console.WriteLine("Engine Started!");
        }
        
        public void Accelerate(int increaseSpeed)
        {
        Speed += increaseSpeed;
        }
        
        public void Brake(int decreaseSpeed)
        {
        Speed -= decreaseSpeed;
                
        }
        
        public void Miles(double miles)
        {
        Mileage = 0.1;
        }
        
        public void Left(int degrees = 40)
        {        
        Console.WriteLine($"you are now {degrees} degrees to the left");
        }
        
        public void Right(int degrees = 35)
        {
        Console.WriteLine($"You are now {degrees} degrees to the right");
        }
        
        public void StopEngine()
        {
        Console.WriteLine("Engine Stopped!");
        }
        
        public string GetMake()
        {
        return Make;
        }
        
        public void SetMake(string newMake)
        {
         Make = newMake;
        }
        public string GetModel()
        {
        return Model;
        }
        
        public void  SetModel(string newModel)
        {
         Model = newModel;
        }
}
class Program
{
    public static void Main(string[] args)
        {
                Car myNewCar = new Car("Tesla", "Model X");
                
                myNewCar.StartEngine();
                myNewCar.Left();
                myNewCar.Right();
                myNewCar.StopEngine();
                
                Console.WriteLine($"Make: {myNewCar.GetMake()} Model: {myNewCar.GetModel()}");
        }
}
