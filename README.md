# Exp03-Constructor
## Aim: 
To write a C# program to calculate the salary of an employee by passing the name, designation, noofexperience, basic salary and insurance amount through constructor.

## Algorithm:
### Step1:
### Step2:
### Step3:
### Step4:
### Step5:
### Step6:

## Program:
```c#
using System;

namespace Exp3
{
    public class Employee
    {
        public string name, designation;
        public int bsalary, noofexp, insurance;
        public float hra, ta, grosspay;

        public Employee(string name, string designation, int bsalary, int noofexp, int insurance)
        {
            this.name = name;
            this.designation = designation;
            this.bsalary = bsalary;
            this.noofexp = noofexp;
            this.insurance = insurance;
        }

        public void CalculateSalary()
        {
            hra = (20 / 100) * bsalary;
            ta = (10 / 100) * bsalary;
            grosspay = bsalary + hra + ta - insurance;
        }

        public void DisplayDetails()
        {
            Console.WriteLine("{0} having {1} yrs of experience, working as a {2}", name, noofexp, designation);
            Console.WriteLine("Receives {0} as his/her salary", grosspay);
        }
    }

    class Program
    {
        static void Main(string[] args)
        {
            string name, designation;
            int bsalary, noofexp, insurance;

            Console.WriteLine("Enter details for Employee 1:");
            Console.Write("Name: ");
            name = Console.ReadLine();
            Console.Write("Designation: ");
            designation = Console.ReadLine();
            Console.Write("Basic Salary: ");
            bsalary = int.Parse(Console.ReadLine());
            Console.Write("Number of years of experience: ");
            noofexp = int.Parse(Console.ReadLine());
            Console.Write("Insurance amount: ");
            insurance = int.Parse(Console.ReadLine());

            Employee emp1 = new Employee(name, designation, bsalary, noofexp, insurance);
            emp1.CalculateSalary();

            Console.WriteLine("\nEnter details for Employee 2:");
            Console.Write("Name: ");
            name = Console.ReadLine();
            Console.Write("Designation: ");
            designation = Console.ReadLine();
            Console.Write("Basic Salary: ");
            bsalary = int.Parse(Console.ReadLine());
            Console.Write("Number of years of experience: ");
            noofexp = int.Parse(Console.ReadLine());
            Console.Write("Insurance amount: ");
            insurance = int.Parse(Console.ReadLine());

            Employee emp2 = new Employee(name, designation, bsalary, noofexp, insurance);
            emp2.CalculateSalary();

            emp1.DisplayDetails();
            emp2.DisplayDetails();

            Console.ReadLine();
        }
    }
}
```


## Output:

![image](https://github.com/vinushcv/Exp03-Constructor/assets/113975318/3df7a7bd-13e8-4032-9eb9-6a7b2d1d8518)


## Result:
