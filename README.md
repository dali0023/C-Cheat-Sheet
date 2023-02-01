# C# Cheat-Sheet

Syntax:
WriteLine or Write:

```c#
Console.WriteLine("Hello "); // Hello
Console.Write("Hello "); // Hello

User Input:
int age = Console.ReadLine();
Console.WriteLine("Your age is: " + age);
```

String Interpolation:

```c#
int x = Int32.Parse(Console.ReadLine());
int y = 10;
string z = $"the addition of {x} + {y} = {x+y}";
Console.WriteLine(z);
```

### Types and variables:

There are two kinds of types in C#:

1. Value types:
   Simple types / primitive Data Types: `short, int, char, float, double` etc. (They are called `primitive` because they
   are the `main built-in types` and could be used to build other data types.), `Enum types, Struct types, Nullable value types`

2. Reference types: `Class types, Interface types, Array types, Delegate types, Object`: You can assign values of any type to variables of type object.

```c#
int myNum = 5; double myDouble = 5.25; float myFloatNum = 5.99f;
string myText = "Hello";char myLetter = 'D'; bool myBool = true;
const int myNum = 15; myNum = 20; // error
int x = 5, y = 6, z = 50;
Console.WriteLine(x + y + z);
var collage = "Algonquin"; var year = 2020; var TuitionFees = 34670.50; // Local Variable/ Implicitly type variable: var
```

### Reference Types:

Class Ref: `Properties, Methods, Events` etc.

```c#
class Employee
   {
       public string Name;
       public string City;
   }

class Program
    {
        public string name;
        // Reference Variable that has two veriable(City, Name)

        static void Main(string[] args)
        {
            Program obj1 = new Program();
            obj1.name = "Algonquin College";
            Console.WriteLine(obj1.name);

            Employee obj2;
            obj2 = new Employee();
            obj2.eName = "Nazmul Hasan";
            Console.WriteLine(obj2.eName);
            Console.ReadLine();
        }
    }
```

# Type Casting/Type Conversion

- is the process to change one data type value into another data type.
  Implicit Casting (automatically) - converting a smaller type to a larger type size `char -> int -> long -> float -> double`

```c#
 int myInt = 9;
 double myDouble = myInt; // Automatic casting: int to double

 Explicit Casting (manually) - converting a larger type to a smaller size type
    double -> float -> long -> int -> char
    double myDouble = 9.78;
    int myInt = (int)myDouble; // Manual casting: double to int

    Console.WriteLine(myDouble); // Outputs 9.78
    Console.WriteLine(myInt); // Outputs 9

    int math = 70; english = 11;
    double total = (double) math/english; // 6.3456788
    int total1 = (int) total; //6
```

# Type Conversion Methods:

```c#
 int myInt = 10;
 double myDouble = 5.25;
 bool myBool = true;

 Console.WriteLine(Convert.ToString(myInt)); // convert int to string
 Console.WriteLine(Convert.ToDouble(myInt)); // convert int to double
 Console.WriteLine(Convert.ToInt32(myDouble)); // convert double to int
 Console.WriteLine(Convert.ToString(myBool)); // convert bool to string
int i = 75;
float f = 53.005f;
double d = 2345.7652;
bool b = true;
Console.WriteLine(i.ToString());
Console.WriteLine(f.ToString());
Console.WriteLine(d.ToString());
Console.WriteLine(b.ToString());

// TryParse: Convert String and return true or false
   string myStr = "Dalim";
   bool res = int.TryParse(myStr, out int x);
   bool res = int.TryParse(myStr, out _);
   Console.WriteLine(res);); // T or F

// Parse: Convert String:
   int x = Int32.Parse(Console.ReadLine());
   int y = 10;
   Console.WriteLine(x + y);
Reference Types:
class types, interface types, delegate types, and array types.

```
