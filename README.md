# GB_Basics
Задачи "Знакомство с языками программирования"

# Задача 1: Напишите программу, которая на вход принимает два числа и проверяет, является ли первое число квадратом второго.
```
Console.Clear();

Console.Write("Введите 1-ое число: ");
int n = Convert.ToInt32(Console.ReadLine());
Console.Write("Введите 2-ое число: ");
int m = Convert.ToInt32(Console.ReadLine());
if (m * m == n)
    Console.WriteLine("yes");
else
    Console.WriteLine("no");
```

# Задача 2: Напишите программу, которая на вход принимает два числа и выдаёт, какое число большее, а какое меньшее.
```
Console.Clear();
Console.WriteLine("Введите число a: ");
int a = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("Введите число b: ");
int b = Convert.ToInt32(Console.ReadLine());

if (a > b)
    Console.WriteLine($"a={a}; b={b} -> max {a} ");
else
    Console.WriteLine($"a={a}; b={b} -> max {b} ");
```

# Задача 3: Напишите программу, которая будет выдавать название дня недели по заданному номеру.
```
Console.Clear();

Console.Write("Введите день недели: ");
int n = Convert.ToInt32(Console.ReadLine());
while (n < 1 || n > 7)
{
    Console.Write("Вы ошиблись!\nВведите день недели: ");
    n = Convert.ToInt32(Console.ReadLine());
}
if (n == 1)
    Console.WriteLine("Понедельник");
else if (n == 2)
    Console.WriteLine("Вторник");
else if (n == 3)
    Console.WriteLine("Среда");
else if (n == 4)
    Console.WriteLine("Четверг");
else if (n == 5)
    Console.WriteLine("Пятница");
else if (n == 6)
    Console.WriteLine("Суббота");
else
    Console.WriteLine("Воскресенье");
```

# Задача 4: Напишите программу, которая принимает на вход три числа и выдаёт максимальное из этих чисел.
```
Console.Clear();
Console.WriteLine("Введите число n1: ");
int n1 = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("Введите число n2: ");
int n2 = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("Введите число n3: ");
int n3 = Convert.ToInt32(Console.ReadLine());

if ((n1 > n2) & (n1 > n3))
    Console.WriteLine($"{n1}, {n2}, {n3} -> {n1} ");
else if (n2 > n3)
    Console.WriteLine($"{n1}, {n2}, {n3} -> {n2} ");
else 
    Console.WriteLine($"{n1}, {n2}, {n3} -> {n3} ");
```

# Задача 5: Напишите программу, которая на вход принимает одно число (N), а на выходе показывает все целые числа в промежутке от -N до N.
```
Console.Clear();

Console.Write("Введите число: ");
int n = Convert.ToInt32(Console.ReadLine()), count = (-1) * n;
for (int i = (-1) * n; i <= n; i++)
    Console.Write($"{i} ");
Console.WriteLine();
while (count <= n)
{
    Console.Write($"{count} ");
    count++; // count = count + 1;
}
```

# Задача 6: Напишите программу, которая на вход принимает число и выдаёт, является ли число чётным (делится ли оно на два без остатка).
```
Console.Clear();
Console.WriteLine("Введите число n: ");
int n = Convert.ToInt32(Console.ReadLine());

if (n % 2 == 0)
    Console.WriteLine($"{n} -> да ");
else
    Console.WriteLine($"{n} -> нет ");
```

# Задача 7: Напишите программу, которая принимает на вход трёхзначное число и на выходе показывает последнюю цифру этого числа.
```
Console.Clear();

Console.Write("Введите число: ");
int n = Convert.ToInt32(Console.ReadLine());
Console.WriteLine(n % 10);
```

# Задача 8: Напишите программу, которая на вход принимает число (N), а на выходе показывает все чётные числа от 1 до N.
```
Console.Clear();
Console.WriteLine("Введите число N от 1: ");
int n = Convert.ToInt32(Console.ReadLine());
string s = "";

while (n < 1)
{
    Console.Write("Вы ошиблись!\nВведите число N от 1: ");
    n = Convert.ToInt32(Console.ReadLine());
}

for (int i = 1; i <= n; i++)
{
    if (i % 2 == 0) 
        s = s + ($"{i } ");
}

Console.WriteLine($"{n} -> {s} ");
```

# Задача 9: Напишите программу, которая выводит случайное число из отрезка [10, 99] и показывает наибольшую цифру числа.
```
Console.Clear();

int n = new Random().Next(10, 100); // [10, 99]
Console.WriteLine(n);
int n1 = n / 10;
int n2 = n % 10;
if (n1 > n2)
    Console.WriteLine(n1);
else
    Console.WriteLine(n2);
```

# Задача 10: Напишите программу, которая принимает на вход трёхзначное число и на выходе показывает вторую цифру этого числа.
```
Console.Clear();
Console.WriteLine("Введите трёхзначное число n: ");
int n = Convert.ToInt32(Console.ReadLine());

while ((n<100) || (n>=1000))
{
    Console.Write("Вы ошиблись!\nВведите трёхзначное число n: ");
    n = Convert.ToInt32(Console.ReadLine());
}
int result = (n / 10) % 10;
Console.WriteLine($"{n} -> {result} ");
```

# Задача 11: Напишите программу, которая выводит случайное трёхзначное число и удаляет вторую цифру этого числа.
```
Console.Clear();

int n = new Random().Next(100, 1000); // [100, 999]
Console.WriteLine(n);
int n1 = n / 100;
int n3 = n % 10;
Console.WriteLine(n1 * 10 + n3);
```

# Задача 12: Напишите программу, которая будет принимать на вход два числа и выводить, является ли второе число кратным первому. Если число 2 не кратно числу 1, то программа выводит остаток от деления.
```
Console.Clear();

Console.Write("Введите 1-ое число: ");
int n = Convert.ToInt32(Console.ReadLine());
Console.Write("Введите 2-ое число: ");
int m = Convert.ToInt32(Console.ReadLine());
if (n % m == 0)
    Console.WriteLine("yes");
else
    Console.WriteLine(n % m);
```

# Задача 13: Напишите программу, которая выводит третью цифру заданного числа или сообщает, что третьей цифры нет.
```
Console.Clear();
Console.WriteLine("Введите число n: ");
int n = Convert.ToInt32(Console.ReadLine());
int d = n;
if (n < 100)
    Console.WriteLine($"{n} -> третьей цифры нет ");
else
{
    while (n > 999)
    {
        n = n / 10;
    }
    int result = n % 10;
    Console.WriteLine($"{d} -> {result} ");
}
```

# Задача 14: Напишите программу, которая принимает на вход число и проверяет, кратно ли оно одновременно 7 и 23.
```
Console.Clear();

Console.Write("Введите число: ");
int n = Convert.ToInt32(Console.ReadLine());
if (n % 161 == 0)
    Console.WriteLine("yes");
else
    Console.WriteLine("no");
```

# Задача 15: Напишите программу, которая принимает на вход цифру, обозначающую день недели, и проверяет, является ли этот день выходным.
```
Console.Clear();
Console.WriteLine("Введите цифру, обозначающую день недели: ");
int n = Convert.ToInt32(Console.ReadLine());

while ((n < 1) || (n >= 8))
{
    Console.Write("Вы ошиблись!\nВведите цифру, обозначающую день недели: ");
    n = Convert.ToInt32(Console.ReadLine());
}
if (n < 6)
    Console.WriteLine($"{n} -> нет ");
else
    Console.WriteLine($"{n} -> да ");
```

# Второй максимум. Дополнительная задача (https://acmp.ru/asp/do/index.asp?main=task&id_course=1&id_section=3&id_topic=35&id_problem=223)
## Задана последовательность натуральных чисел, завершающаяся числом 0. Требуется определить значение второго по величине элемента в этой последовательности, то есть элемента, который будет наибольшим, если из последовательности удалить наибольший элемент.
```
Console.Clear();
int n = Convert.ToInt32(Console.ReadLine());
int m1 = 0;
int m2 = 0;
string s = "";
while (n != 0)
{
    if (n >= m1)
    {
        m2 = m1;
        m1 = n;
    }
    else if ((m2 < n) & (n < m1))
        m2 = n;

    s = s + ($"{n} ");
    n = Convert.ToInt32(Console.ReadLine());
}
Console.WriteLine($"{s} -> {m2} ");
```

# Задача 16: Напишите программу, которая принимает на вход два числа и проверяет, является ли одно число квадратом другого.
```
Console.Clear();

Console.Write("Введите 1-ое число: ");
int n = Convert.ToInt32(Console.ReadLine());
Console.Write("Введите 2-ое число: ");
int m = Convert.ToInt32(Console.ReadLine());
if (n * n == m || m * m == n)
    Console.WriteLine("yes");
else
    Console.WriteLine("no");
```

# Задача 17: Напишите программу, которая принимает на вход координаты точки (X и Y), причём X ≠ 0 и Y ≠ 0 и выдаёт номер четверти плоскости, в которой находится эта точка.
```
Console.Clear();
Console.Write("Введите координату X: ");
double x = Convert.ToDouble(Console.ReadLine());
Console.Write("Введите координату Y: ");
double y = Convert.ToDouble(Console.ReadLine());
while (x == 0)
{
  Console.Write("Вы ошиблись!\nВведите координату X: ");
  x = Convert.ToDouble(Console.ReadLine());
}
while (y == 0)
{
  Console.Write("Вы ошиблись!\nВведите координату Y: ");
  y = Convert.ToDouble(Console.ReadLine());
}
if (x > 0 && y > 0)
  Console.WriteLine("I");
else if (x < 0 && y > 0)
  Console.WriteLine("II");
else if (x < 0 && y < 0)
  Console.WriteLine("III");
else
  Console.WriteLine("IV");
```

# Задача 18: Напишите программу, которая по заданному номеру четверти, показывает диапазон возможных координат точек в этой четверти (x и y).
```
Console.Clear();
Console.Write("Введите номер четверти: ");
int n = Convert.ToInt32(Console.ReadLine());
while (n < 1 || n > 4)
{
  Console.Write("Вы ошиблись!\nВведите номер четверти: ");
  n = Convert.ToInt32(Console.ReadLine());
}
if (n == 1)
  Console.WriteLine("x ∈ (0; +∞) and y ∈ (0; +∞)");
else if (n == 2)
  Console.WriteLine("x ∈ -∞; 0 and y ∈ 0; +∞");
else if (n == 3)
  Console.WriteLine("x ∈ -∞; 0 and y ∈ -∞; 0");
else
  Console.WriteLine("x ∈ (0; +∞) and y ∈ (-∞; 0)");
```

# Задача 19: Напишите программу, которая принимает на вход пятизначное число и проверяет, является ли оно палиндромом.
```
Console.Write("Введите число: ");
int n = Convert.ToInt32(Console.ReadLine());
string s = Convert.ToString(n);
while (s.Length!=5)
{
    Console.Write($"Вы ошиблись! {s.Length}\nВведите пятизначное число: ");
    n = Convert.ToInt32(Console.ReadLine());
    s = Convert.ToString(n);
}

if ((s[0] == s[4]) & (s[1] == s[3]))
    Console.WriteLine($"Число {n} -> палиндром");
else
    Console.WriteLine($"Число {n} -> не палиндром");
```

# Задача 20:
```
```

# Задача 21: Напишите программу, которая принимает на вход координаты двух точек и находит расстояние между ними в 3D пространстве.
```
Console.Clear();       
Console.Write("Введите координату x1: ");
double x1 = Convert.ToDouble(Console.ReadLine());
Console.Write("Введите координату y1: ");
double y1 = Convert.ToDouble(Console.ReadLine());
Console.Write("Введите координату z1: ");
double z1 = Convert.ToDouble(Console.ReadLine());
Console.Write("Введите координату x2: ");
double x2 = Convert.ToDouble(Console.ReadLine());
Console.Write("Введите координату y2: ");
double y2 = Convert.ToDouble(Console.ReadLine());
Console.Write("Введите координату z2: ");
double z2 = Convert.ToDouble(Console.ReadLine());

double s = Math.Sqrt(Math.Pow(x2 - x1, 2) + Math.Pow(y2 - y1, 2) + Math.Pow(z2 - z1, 2));
Console.WriteLine($"A({x1},{y1},{z1}); B({x2},{y2},{z2}), -> {Math.Round(s, 2)}");
```

# Задача 22: Напишите программу, которая принимает на вход число (N) и выдаёт таблицу квадратов чисел от 1 до N.
```
Console.Clear();
Console.Write("Введите число: ");
int n = Convert.ToInt32(Console.ReadLine());
for (int i = 1; i <= n; i++)
  Console.WriteLine($"{i} ^ 2 = {i * i} ");


Console.Clear();
Console.Write("Введите число: ");
int n = Convert.ToInt32(Console.ReadLine());
for (int i = 1; i <= n; i++)
  Console.Write($"{i * i} ");
```

# Задача 23: Напишите программу, которая принимает на вход число (N) и выдаёт таблицу кубов чисел от 1 до N.
```
Console.Clear();  
Console.WriteLine("Введите число N: ");
int n = Convert.ToInt32(Console.ReadLine());
string s = "";
for (int i = 1; i <= n; i++)
{
    s = s + ($"{i * i * i} ");
}
Console.WriteLine($"{n} -> {s} ");
```

# Сбор черники. Дополнительная задача(https://acmp.ru/asp/do/index.asp?main=task&id_course=1&id_section=5&id_topic=113&id_problem=695)
## В фермерском хозяйстве в Карелии выращивают чернику. Она растет на круглой грядке, причем кусты высажены только по окружности. Таким образом, у каждого куста есть ровно два соседних. Всего на грядке растет N кустов. Эти кусты обладают разной урожайностью, поэтому ко времени сбора на них выросло различное число ягод – на i-ом кусте выросло ai ягод. В этом фермерском хозяйстве внедрена система автоматического сбора черники. Эта система состоит из управляющего модуля и нескольких собирающих модулей. Собирающий модуль за один заход, находясь непосредственно перед некоторым кустом, собирает ягоды с этого куста и с двух соседних с ним. Напишите программу для нахождения максимального числа ягод, которое может собрать за один заход собирающий модуль, находясь перед некоторым кустом заданной во входном файле грядки.
```
Console.Clear();
Console.WriteLine("Введите количество кустов: ");
int n = Convert.ToInt32(Console.ReadLine());

while ((n < 3) || (n > 1000))
{
    Console.WriteLine($"Вы ошиблись! Количество кустов не должно быть меньше 3-х или больше 1000! \nВведите количество кустов: ");
    n = Convert.ToInt32(Console.ReadLine());
}
int[] numbers = new int[n];

for (int i = 0; i < n; i++)
{
    Console.WriteLine($"Введите количество ягод на кусту {i + 1}: ");
    numbers[i] = Convert.ToInt32(Console.ReadLine());
}

int max = 0;
int s1 = 0;
int s2 = 0;
int s3 = 0;
for (int i = 1; i < numbers.Length-1; i++)
{
    s1 = numbers[i-1] + numbers[i] + numbers[i+1];
    if (s1 > max)
        max = s1;
    else if (s1 >= 1000)
        max = 1000;
    s2 = numbers[numbers.Length-1] + numbers[0] + numbers[i];    
    if (s2 > max)
        max = s2;
    else if (s2 >= 1000)
        max = 1000;
    s3 = numbers[numbers.Length-2] + numbers[numbers.Length-1] + numbers[0];    
    if (s3 > max)
        max = s3;    
    else if (s3 >= 1000)
        max = 1000;
}

Console.WriteLine($"Максимального числа ягод, которое может собрать за один заход собирающий модуль: {max}");
```
# Задача 24: Напишите программу, которая принимает на вход число (А) и выдаёт сумму чисел от 1 до А.
```
﻿// Задача №24
// Напишите программу, которая принимает на вход число (А) и выдаёт сумму чисел от 1 до А.

//Метод читает данные от пользователя
int ReadData(string msg)
{
    Console.WriteLine(msg);
    return int.Parse(Console.ReadLine() ?? "0");
}
//Выводим результат пользователю
void PrintData(string msg1, int msg2)
{
    Console.WriteLine(msg1);
    Console.WriteLine(msg2);
}

int SumSimple(int numA)
{ 
    int sumOfNum = 1;
    for(int i=2;i<=numA;i++)
    {
        sumOfNum+=i;
    }
    return sumOfNum;
}

int SumGauss(int numA)
{
    return (numA*(numA+1))/2;
}

int numberA = ReadData("Введите число A");

DateTime d1 = DateTime.Now;
int res1 = SumSimple(numberA);
Console.WriteLine(DateTime.Now - d1);

DateTime d2 = DateTime.Now;
int res2 = SumGauss(numberA);
Console.WriteLine(DateTime.Now - d2);

PrintData("Сумма чисел от 1 до А(SumSimple): ",res1);
PrintData("Сумма чисел от 1 до А(SumGauss): ",res2);
```

# Задача 25: Напишите цикл, который принимает на вход два числа (A и B) и возводит число A в натуральную степень B.
Нельзя использовать Math.Pow();
```
Console.Clear();
Console.Write("Введите число A: ");
int a = Convert.ToInt32(Console.ReadLine());
Console.Write("Введите степень B: ");
int b = Convert.ToInt32(Console.ReadLine());

int result = 1;
for (int i = 1; i <= b; i++)
    result = result * a;
Console.WriteLine($"{a},{b} -> {result} ({a}^{b})");
```

# Задача 26: Напишите программу, которая принимает на вход число и выдаёт количество цифр в числе.
```
//Метод читает данные от пользователя
int ReadData(string msg)
{
    Console.WriteLine(msg);
    return int.Parse(Console.ReadLine() ?? "0");
}
//Выводим результат пользователю
void PrintData(string msg1, int msg2)
{
    Console.WriteLine(msg1);
    Console.WriteLine(msg2);
}

int SumDigit(int num)
{
    int res =0;
    while(num>0)
    {
        res++;
        num=num/10;
    }
    return res;
}

int SumDigStr(int num)
{
    int res =0;
    res = num.ToString().Length;
    return res; 
}

int VariantLog(int num)
{
    int count = (int)Math.Log10(num)+1;
    return count;
}

int number = ReadData("Введите число: ");

DateTime d1 = DateTime.Now;
int res1 = SumDigit(number);
Console.WriteLine(DateTime.Now - d1);
PrintData("Вариант (SumDigit): ",res1);

DateTime d2 = DateTime.Now;
int res2 = SumDigStr(number);
Console.WriteLine(DateTime.Now - d2);
PrintData("Вариант (SumDigStr): ",res2);

DateTime d3 = DateTime.Now;
int res3 = VariantLog(number);
Console.WriteLine(DateTime.Now - d3);
PrintData("Вариант (VariantLog): ",res3);
```

# Задача 27: Напишите программу, которая принимает на вход число и выдаёт сумму цифр в числе.
```
Console.Clear();
Console.Write("Введите число N: ");
int n = Convert.ToInt32(Console.ReadLine());

int result = 0;
while (n != 0)
{
    result = result + n % 10;
    n = n / 10;
}

Console.WriteLine($"Сумма цифр в числе N -> {result}");
```

# Задача 28: Напишите программу, которая принимает на вход число N и выдаёт произведение чисел от 1 до N.
```
Console.Clear();
using System.Numerics;

//Метод читает данные от пользователя
int ReadData(string msg)
{
    Console.WriteLine(msg);
    return int.Parse(Console.ReadLine() ?? "0");
}
//Выводим результат пользователю
void PrintData(string msg1, BigInteger msg2)
{
    Console.WriteLine(msg1);
    Console.WriteLine(msg2);
}

BigInteger CalcFact(int num)
{
    BigInteger res=1;
    for(int i=1;i<=num;i++)
    {
        res=res*i;
    }
    return res;
}

int number = ReadData("Введите число:");

BigInteger fact = CalcFact(number);

PrintData("Факториал равен: ",fact);
```

# Задача 29: https://acmp.ru/asp/do/index.asp?main=task&id_course=1&id_section=5&id_topic=114&id_problem=699
## Петя впервые пришел на урок физкультуры в новой школе. Перед началом урока ученики выстраиваются по росту, в порядке невозрастания. Напишите программу, которая определит на какое место в шеренге Пете нужно встать, чтобы не нарушить традицию, если заранее известен рост каждого ученика и эти данные уже расположены по невозрастанию (то есть каждое следующее число не больше предыдущего). Если в классе есть несколько учеников с таким же ростом, как у Пети, то программа должна расположить его после них.
```
Console.Clear();
Console.Write("Введите число учеников: ");
int n1 = Convert.ToInt32(Console.ReadLine());

while (n1 > 100)
{
    Console.WriteLine($"Вы ошиблись! Максимальное число учеников не должно превышать 100! \nВведите количество учеников: ");
    n1 = Convert.ToInt32(Console.ReadLine());
}

Console.Write("Введите рост Пети: ");
int n2 = Convert.ToInt32(Console.ReadLine());
while (n2 > 200)
{
    Console.WriteLine($"Вы ошиблись! Рост Пети не должен превышать 200! \nВведите рост Пети: ");
    n2 = Convert.ToInt32(Console.ReadLine());
}

int[] array = new int[n1];
for (int i = 0; i < n1; i++)
{
    array[i] = new Random().Next(100, 200); 
}

int result = 0;
for (int i = 0; i < n1; i++)
{
    if (array[i] > n2)
    {
        result = result + 1;
    }
}

Console.WriteLine($"Рост учеников: [{string.Join(", ", array)}] ");
Console.WriteLine($"Количество учеников выше Пети: {result} ");
```

# Суперсдвиг. (https://acmp.ru/asp/do/index.asp?main=task&id_course=1&id_section=5&id_topic=114&id_problem=702)
## Дана последовательность из N целых чисел и число K. Необходимо сдвинуть всю последовательность (сдвиг - циклический) на |K| элементов вправо, если K – положительное и влево, если отрицательное.
```
Console.Clear();
Console.Write("Введите количество чисел N: ");
int n = Convert.ToInt32(Console.ReadLine());

Console.Write("Введите число K: ");
int k = Convert.ToInt32(Console.ReadLine());

int[] array = new int[n];
for (int i = 0; i < n; i++)
    array[i] = new Random().Next(0, 9); 

int[] result = new int[n];
for(int i = 0; i < n; i++)
    result[i] = array[(i - k + n) % n];

Console.WriteLine($"Первоначальная последовательность чисел: [{string.Join(", ", array)}] ");
Console.WriteLine($"Последовательность чисел после перестановки: [{string.Join(", ", result)}] ");
```

# Гипотеза Гольдбаха. (https://acmp.ru/asp/do/index.asp?main=task&id_course=1&id_section=6&id_topic=117&id_problem=723)
## Известно, что любое чётное число, большее 2, представимо в виде суммы 2 простых чисел, причём таких разложений может быть несколько. Впервые гипотезу о существовании данного разложения сформулировал математик Х. Гольдбах. Требуется написать программу, производящую согласно утверждению Гольдбаха, разложение заданного чётного числа. Из всех пар простых чисел, сумма которых равна заданному числу, требуется найти пару, содержащую наименьшее простое число.
```
Console.Clear();
Console.Write("Введите четное число N: ");
int n = Convert.ToInt32(Console.ReadLine());
while (((n < 4) || (n > 999)) || (n % 2==1))
{
    Console.WriteLine($"Вы ошиблись!\nВведите четное число больше 3-х или больше 998! ");
    n = Convert.ToInt32(Console.ReadLine());
}

bool f(int N)
{
    bool flag = true;
    for (int j = 2; j < N - 1; j++)
        if (N % j == 0)
            flag = false;
    return flag;
}

bool check  = true;
int n1 = 0;
int n2 = 0;
int i = 1;
while ((i < n / 2 + 1) && (check))
{
    if(f(i) && f(n - i))
    {
        n1 = i;
        n2 = n - i;

        if (n1 > 1)
            check = false;
    } 
    i++;
}

Console.WriteLine($"Результат: {n1}, {n2} ");
```

# Задача 30: Напишите программу, которая выводит массив из 8 элементов, заполненный нулями и единицами в случайном порядке.
```
Console.Clear();
int InputNum(string msg)
{
    Console.Write(msg);
    return int.Parse(Console.ReadLine() ?? "0");
}
int xlen = InputNum("Ваше число X: ");
int ylen = InputNum("Ваше число Y: ");
Random rnd = new Random();
int[,] createArray(int xlen, int ylen)
{
    int[,] arr = new int[xlen, ylen];
    for (int i = 0; i < xlen; i++)
    {
        for (int j = 0; j < ylen; j++)
        {
            arr[i, j] = rnd.Next(-999, 999);
        }
    }
    return arr;
}
void showArray(int[,] arr)
{
    for (int i = 0; i < xlen; i++)
    {
        for (int j = 0; j < ylen; j++)
        {
            
        Console.Write(arr[i,j]+"\t");
        }
        Console.WriteLine("");
    }
}
showArray(createArray(xlen, ylen));
```

# Задача 31: Задайте массив из 12 элементов, заполненный случайными числами из промежутка [-9, 9]. Найдите сумму отрицательных и положительных элементов массива.
```
void InputArray(int[] array)
{
  for (int i = 0; i < array.Length; i++)
    array[i] = new Random().Next(-9, 10); // [-9, 9]
}


void ReleaseArray(int[] array)
{
  int summaPositive = 0, summaNegative = 0;
  foreach (int i in array)
  {
    if (i > 0)
      summaPositive += i;
    else
      summaNegative += i;
  }
  Console.WriteLine($"Сумма положительных чисел равна {summaPositive}");
  Console.WriteLine($"Сумма отрицательных чисел равна {summaNegative}");
}


Console.Clear();
int[] array = new int[12];
InputArray(array);
Console.WriteLine($"Начальный массив: [{string.Join(", ", array)}]");
ReleaseArray(array);
```

# Задача 32: Напишите программу замена элементов массива: положительные элементы замените на соответствующие отрицательные, и наоборот.
```
void InputArray(int[] array)
{
  for (int i = 0; i < array.Length; i++)
    array[i] = new Random().Next(-9, 10); // [-9, 9]
}


void ReleaseArray(int[] array)
{
  for (int i = 0; i < array.Length; i++)
    array[i] *= (-1);
}


Console.Clear();
Console.Write("Введите кол-во элементов: ");
int n = Convert.ToInt32(Console.ReadLine());
int[] array = new int[n];
InputArray(array);
Console.WriteLine($"Начальный массив: [{string.Join(", ", array)}]");
ReleaseArray(array);
Console.WriteLine($"Конечный массив: [{string.Join(", ", array)}]");
```

# Задача 33: Задайте массив. Напишите программу, которая определяет, присутствует ли заданное число в массиве.
```
void InputArray(int[] array)
{
  for (int i = 0; i < array.Length; i++)
    array[i] = new Random().Next(-9, 10); // [-9, 9]
}


string ReleaseArray(int[] array, int k)
{
  foreach (int element in array)
  {
    if (element == k)
      return "yes";
  }
  return "no";
}


Console.Clear();
Console.Write("Введите кол-во элементов: ");
int n = Convert.ToInt32(Console.ReadLine());
int[] array = new int[n];
InputArray(array);
Console.WriteLine($"Начальный массив: [{string.Join(", ", array)}]");
Console.Write("Введите число, которое Вы хотите найти: ");
int k = Convert.ToInt32(Console.ReadLine());
Console.WriteLine(ReleaseArray(array, k));
```

# Задача 34: Задайте массив заполненный случайными положительными трёхзначными числами. Напишите программу, которая покажет количество чётных чисел в массиве.
```
void InputArray(int[] array)
{
    for (int i = 0; i < array.Length; i++)
        array[i] = new Random().Next(100, 999);
}

int NumberEven(int[] array)
{
    int nummaEven = 0;
    foreach (int i in array)
    {
        if (i % 2==0)
            nummaEven ++;
    }
    return nummaEven;
}

Console.Clear();
Console.Write("Введите кол-во элементов: ");
int n = Convert.ToInt32(Console.ReadLine());
int[] array = new int[n];
InputArray(array);
int s = NumberEven(array);
Console.WriteLine($"Количество чётных чисел в массиве: [{string.Join(", ", array)}] -> {s} ");
```

# Задача 35: Задайте одномерный массив из 123 случайных чисел. Найдите количество элементов массива, значения которых лежат в отрезке [10,99]. 
```
void InputArray(int[] array)
{
  for (int i = 0; i < array.Length; i++)
    array[i] = new Random().Next(-100, 101); // [-100, 100]
}


int ReleaseArray(int[] array)
{
  int count = 0;
  foreach (int element in array)
  {
    if (element >= 10 && element <= 99)
      count++; // count = count + 1;
  }
  return count;
}


Console.Clear();
// Console.Write("Введите кол-во элементов: ");
// int n = Convert.ToInt32(Console.ReadLine());
int[] array = new int[123];
InputArray(array);
Console.WriteLine($"Начальный массив: [{string.Join(", ", array)}]");
Console.WriteLine(ReleaseArray(array));
```

# Задача 36: Задайте одномерный массив, заполненный случайными числами. Найдите сумму элементов, стоящих на нечётных позициях.
```
void InputArray(int[] array)
{
    for (int i = 0; i < array.Length; i++)
        array[i] = new Random().Next(-100, 100);
}

int SummaUneven(int[] array)
{
    int summaUneven = 0;
    for (int i = 1; i < array.Length; i+=2)
        summaUneven += array[i];
    return summaUneven;
}

Console.Clear();
Console.Write("Введите кол-во элементов: ");
int n = Convert.ToInt32(Console.ReadLine());
int[] array = new int[n];
InputArray(array);
int s = SummaUneven(array);
Console.WriteLine($"Сумма элементов, стоящих на нечётных позициях: [{string.Join(", ", array)}] -> {s} ");
```

# Задача 37: Найдите произведение пар чисел в одномерном массиве. Парой считаем первый и последний элемент, второй и предпоследний и т.д. Результат запишите в новом массиве.
```
void InputArray(int[] array)
{
  for (int i = 0; i < array.Length; i++)
    array[i] = new Random().Next(1, 11); // [1, 10]
}


void ReleaseArray(int[] array, int[] result)
{
  for (int i = 0; i < result.Length; i++)
    result[i] = array[i] * array[array.Length - 1 - i];
}


Console.Clear();
Console.Write("Введите кол-во элементов: ");
int n = Convert.ToInt32(Console.ReadLine());
int[] array = new int[n];
int[] result = new int[n / 2 + n % 2];
InputArray(array);
Console.WriteLine($"Начальный массив: [{string.Join(", ", array)}]");
ReleaseArray(array, result);
Console.WriteLine($"Конечный массив: [{string.Join(", ", result)}]");
```

# Задача 38: Задайте массив вещественных(дробных) чисел. Найдите разницу между максимальным и минимальным элементов массива.
```
void InputArray(double[] array)
{
    for (int i = 0; i < array.Length; i++)
        array[i] = new Random().Next(-100*100, 100*100)/100.0;
}

Console.Clear();
Console.Write("Введите кол-во элементов: ");
int n = Convert.ToInt32(Console.ReadLine());
double[] array = new double[n];
InputArray(array);
double min = 0;
double max = 0;
foreach (double i in array)  // Поиск максимального и минимального значения
{
    if (min > i) min = i;
    if (max < i) max = i;
}
double result = max - min;
Console.WriteLine($"Разница между максимальной и минимальным элементом массива: [{string.Join("; ", array)}] -> {Math.Round(result, 2)} ");
```

# Статистика. Массивы(https://acmp.ru/asp/do/index.asp?main=task&id_course=1&id_section=5&id_topic=114&id_problem=703)
## Вася не любит английский язык, но каждый раз старается получить хотя бы четверку за четверть, чтобы оставаться ударником. В текущей четверти Вася заметил следующую закономерность: по нечетным дням месяца он получал тройки, а по четным – четверки. Так же он помнит, в какие дни он получал эти оценки. Поэтому он выписал на бумажке все эти дни для того, чтобы оценить, сколько у него троек и сколько четверок. Помогите Васе это сделать, расположив четные и нечетные числа в разных строчках. Вася может рассчитывать на оценку 4, если четверок не меньше, чем троек.
```
void InputArray(int[] array)
{
    for (int i = 0; i < array.Length; i++)
        array[i] = new Random().Next(1, 31);
}

Console.Clear();
Console.Write("Введите кол-во элементов: ");
int n = Convert.ToInt32(Console.ReadLine());
while ((n < 1) || (n > 100))
{
    Console.WriteLine($"Вы ошиблись! Количество элементов целочисленного массива не должно быть меньше 1 и превышать 100! \nВведите кол-во элементов: ");
    n = Convert.ToInt32(Console.ReadLine());
}

int[] array = new int[n];
InputArray(array);
Console.WriteLine($"Начальный массив: [{string.Join(" ", array)}]");

int summaEven = 0;
int summaUneven = 0;
foreach (int i in array)
{
    if (i % 2==0)
        summaEven ++;
    else
        summaUneven ++;
}

int[] arrayThrees = new int[summaUneven];
int[] arrayFours = new int[summaEven];
int n1 = 0;
int n2 = 0;
foreach (int i in array)
{
    if (i % 2==0)
    {   
        arrayFours[n1] = i;
        n1++;
    }
    else
    {
        arrayThrees[n2] = i;
        n2++;
    }
}

Console.WriteLine($"Дни в которые Вася получил тройки: [{string.Join(" ", arrayThrees)}]");
Console.WriteLine($"Дни в которые Вася получил четверки: [{string.Join(" ", arrayFours)}]");

string result = "YES";
if (arrayThrees.Length > arrayFours.Length)
{
    result = "NO";
}
Console.WriteLine($"Расчитывать результат английского языка на 4? {result}");
```

# Задача 39: Напишите программу, которая перевернёт одномерный массив (последний элемент будет на первом месте, а первый - на последнем и т.д.)
```
void InputArray(int[] array)
{
  for (int i = 0; i < array.Length; i++)
    array[i] = new Random().Next(1, 11); // [1, 10]
}

void ReverseArray(int[] array)
{
  for (int i = 0; i < array.Length / 2; i++)
  {
    int temp = array[i];
    array[i] = array[array.Length - 1 - i];
    array[array.Length - 1 - i] = temp;
  }
}

Console.Clear();
Console.Write("Введите кол-во элементов массива: ");
int n = Convert.ToInt32(Console.ReadLine());
int[] array = new int[n];
InputArray(array);
Console.WriteLine($"Начальный массив: [{string.Join(", ", array)}]");
ReverseArray(array);
Console.WriteLine($"Конечный массив: [{string.Join(", ", array)}]");
```

# Задача 40: Напишите программу, которая принимает на вход три числа и проверяет, может ли существовать треугольник с сторонами такой длины.
```
Console.Clear();
Console.Write("Введите длину 1-ой стороны треугольника: ");
int a = Convert.ToInt32(Console.ReadLine());
Console.Write("Введите длину 2-ую стороны треугольника: ");
int b = Convert.ToInt32(Console.ReadLine());
Console.Write("Введите длину 3-ю стороны треугольника: ");
int c = Convert.ToInt32(Console.ReadLine());
if (a + b > c && b + c > a && a + c > b)
  Console.WriteLine("yes");
else
  Console.WriteLine("no");
```

# Задача 41: Пользователь вводит с клавиатуры M чисел. Посчитайте, сколько чисел больше 0 ввёл пользователь.
```
Console.Clear();
Console.Write("Введите количество чисел M, которое вы будете вводить: ");
int m = Convert.ToInt32(Console.ReadLine());

int[] array = new int[m];
int s = 0;
for (int i = 0; i < m; i++)
{
    Console.Write($"Введите число N{i + 1}: ");
    int n = Convert.ToInt32(Console.ReadLine());
    array[i] = n;
    if (n > 0)
        s++;
}

Console.WriteLine($"Количество чисел больше: [{string.Join(", ", array)}] -> {s} ");
```

# Задача 42: Напишите программу, которая будет преобразовывать десятичное число в двоичное.
```
Console.Clear();
Console.Write("Введите число: ");
int n = Convert.ToInt32(Console.ReadLine());
string result = String.Empty;
while (n > 0)
{
  result = Convert.ToString(n % 2) + result;
  n = n / 2;
}
Console.WriteLine(result);
```

# Задача 43: Напишите программу, которая найдёт точку пересечения двух прямых, заданных уравнениями y = k1 * x + b1, y = k2 * x + b2; значения b1, k1, b2 и k2 задаются пользователем.
```
Console.Clear();
Console.Write("Введите значение b1: ");
double b1 = Convert.ToDouble(Console.ReadLine());
Console.Write("Введите значение k1: ");
double k1 = Convert.ToDouble(Console.ReadLine());
Console.Write("Введите значение b2: ");
double b2 = Convert.ToDouble(Console.ReadLine());
Console.Write("Введите значение k2: ");
double k2 = Convert.ToDouble(Console.ReadLine());

double x = Math.Round(((b2 - b1) / (k1 - k2)), 2);
double y = Math.Round((k1 * x + b1), 2);

Console.WriteLine($"b1={b1}, k1={k1}, b2={b2}, k2={k2} -> ({x};{y}) ");
```

# Задача 44: Не используя рекурсию, выведите первые N чисел Фибоначчи. Первые два числа Фибоначчи: 0 и 1.
```
Console.Clear();
Console.Write("Введите число: ");
int n = Convert.ToInt32(Console.ReadLine()), a0 = 0, a1 = 1, x;
for (int i = 0; i < n; i++)
{
  Console.Write($"{a0} ");
  x = a0 + a1;
  a0 = a1;
  a1 = x;
}
```

# Задача 45: Напишите программу, которая будет создавать копию заданного массива с помощью поэлементного копирования.
```
```

# Задача 46: Задайте двумерный массив размером m×n, заполненный случайными целыми числами.
```
void InputMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            matrix[i, j] = new Random().Next(1, 21); // [1, 20]
    }
}

void PrintMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            Console.Write($"{matrix[i, j]} \t");
        Console.WriteLine();
    }
}


Console.Clear();
Console.Write("Введите размер массива: ");
int[] size = Console.ReadLine().Split().Select(x => int.Parse(x)).ToArray();
int[,] matrix = new int[size[0], size[1]];
InputMatrix(matrix);
PrintMatrix(matrix);
```

# Перестановки (Рекурсия). (https://acmp.ru/asp/do/index.asp?main=task&id_course=1&id_section=9&id_topic=123&id_problem=765)
## Дана строка, состоящая из N попарно различных символов. Требуется вывести все перестановки символов данной строки.
```
Console.Clear();
Console.Write("Введите строку состоящую из N символов: ");
string N = Console.ReadLine();
while ((N.Length < 2) || (N.Length > 8))
{
    Console.WriteLine($"Вы ошиблись! Максимальное кол-во символов не должно превышать 8 и не должно быть меньше 1! \nВведите строку состоящую из N символов: ");
    N = Console.ReadLine();
}

char[] ch = new char[N.Length]; 
for (int s = 0; s < N.Length; s++) 
{ 
    ch[s] = N[s]; 
} 

void Permutations(char[] str, int i, int n)
{
    if (str[i] == str[n - 1])
    {
        Console.WriteLine($"Результат: {string.Join("", str)};");
        return;
    }

    for (int j = i; j < n; j++)
    {
        (str[i], str[j]) = (str[j], str[i]);
        Permutations(str, i + 1, n);
        (str[i], str[j]) = (str[j], str[i]);       
    }
}

Permutations(ch, 0, N.Length);
```

# Площадь треугольника. (https://acmp.ru/asp/do/index.asp?main=task&id_course=1&id_section=6&id_topic=116&id_problem=719)
## По целочисленным координатам вершин треугольника (x1,y1), (x2,y2) и (x3,y3) требуется вычислить его площадь.
```
Console.Clear();
string k = "";
Console.Write("Введите координата x1 вершины угла А: ");
int x1 = Convert.ToInt32(Console.ReadLine());
k = k + x1 + " ";
Console.Write("Введите координата y1 вершины угла А: ");
int y1 = Convert.ToInt32(Console.ReadLine());
k = k + y1 + " ";
Console.Write("Введите координата x2 вершины угла B: ");
int x2 = Convert.ToInt32(Console.ReadLine());
k = k + x2 + " ";
Console.Write("Введите координата y2 вершины угла B: ");
int y2 = Convert.ToInt32(Console.ReadLine());
k = k + y2 + " ";
Console.Write("Введите координата x3 вершины угла C: ");
int x3 = Convert.ToInt32(Console.ReadLine());
k = k + x3 + " ";
Console.Write("Введите координата y3 вершины угла C: ");
int y3 = Convert.ToInt32(Console.ReadLine());
k = k + y3;

double a = Math.Sqrt(Math.Pow((x2 - x1), 2) + Math.Pow((y2 - y1), 2));
double b = Math.Sqrt(Math.Pow((x3 - x2), 2) + Math.Pow((y3 - y2), 2));
double c = Math.Sqrt(Math.Pow((x1 - x3), 2) + Math.Pow((y1 - y3), 2));
double p = (a + b + c) / 2.0;
double s = Math.Sqrt(p * (p - a) * (p - b) * (p - c));

Console.WriteLine($"{k}: {Math.Round(s, 2)}");
```

# Задача 47. Задайте двумерный массив размером m×n, заполненный случайными вещественными числами.
```
void InputMatrix(double[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            matrix[i, j] = new Random().Next(-10*100, 10*100)/100.0;
    }
}

void PrintMatrix(double[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            Console.Write($"{matrix[i, j]} \t");
        Console.WriteLine();
    }
}

Console.Clear();
Console.Write("Введите размер массива: ");
int[] size = Console.ReadLine().Split().Select(x => int.Parse(x)).ToArray();
double[,] matrix = new double[size[0], size[1]];
Console.WriteLine("Двумерный массив:");
InputMatrix(matrix);
PrintMatrix(matrix);
```

# Задача 48. Задайте двумерный массив размера m на n, каждый элемент в массиве находится по формуле: Aₘₙ = m+n. Выведите полученный массив на экран.
```
void InputMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            matrix[i, j] = i + j;
    }
}

void PrintMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            Console.Write($"{matrix[i, j]} \t");
        Console.WriteLine();
    }
}

Console.Clear();
Console.Write("Введите размер массива: ");
int[] size = Console.ReadLine().Split().Select(x => int.Parse(x)).ToArray();
int[,] matrix = new int[size[0], size[1]];
InputMatrix(matrix);
PrintMatrix(matrix);
```

# Задача 49. Задайте двумерный массив размера m на n, каждый элемент в массиве находится по формуле: Aₘₙ = m+n. Выведите полученный массив на экран.
```
void InputMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            matrix[i, j] = new Random().Next(1, 21); // [1, 20]
    }
}

void PrintMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            Console.Write($"{matrix[i, j]} \t");
        Console.WriteLine();
    }
}

void CheckOddPosition(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
        {
            if (i % 2 == 1 && j % 2 == 1)
            {
                Console.WriteLine($"{matrix[i, j]} ({i}, {j})");
                matrix[i, j] *= matrix[i, j];
            }
        }
    }
}

Console.Clear();
Console.Write("Введите размер массива: ");
int[] size = Console.ReadLine().Split().Select(x => int.Parse(x)).ToArray();
int[,] matrix = new int[size[0], size[1]];
Console.WriteLine("Начальный массив:");
InputMatrix(matrix);
PrintMatrix(matrix);
Console.WriteLine("Конечный массив:");
CheckOddPosition(matrix);
PrintMatrix(matrix);
```

# Задача 50. Напишите программу, которая на вход принимает позиции элемента в двумерном массиве, и возвращает значение этого элемента или же указание, что такого элемента нет.
```
void InputMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            matrix[i, j] = new Random().Next(-10, 10);
    }
}

void PrintMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            Console.Write($"{matrix[i, j]} \t");
        Console.WriteLine();
    }
}

Console.Clear();
Console.Write("Введите размер массива: ");
int[] size = Console.ReadLine().Split().Select(x => int.Parse(x)).ToArray();
int[,] matrix = new int[size[0], size[1]];
Console.WriteLine("Двумерный массив:");
InputMatrix(matrix);
PrintMatrix(matrix);
Console.Write("Введите позицию массива: ");
int[] poz = Console.ReadLine().Split().Select(x => int.Parse(x)).ToArray();

if (poz[0] < 0 || poz[0] > matrix.GetLength(0)-1 || poz[1] < 0 || poz[1] > matrix.GetLength(1)-1)
{
    Console.WriteLine($"{poz[0]}, {poz[1]} -> Такой позиции в массиве нет");
}
else
{
    Console.WriteLine($"{poz[0]}, {poz[1]} -> {matrix[poz[0], poz[1]]}");
}
```

# Задача 51. Задайте двумерный массив. Найдите элементы, у которых оба индекса чётные, и замените эти элементы на их квадраты.
```
void InputMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            matrix[i, j] = new Random().Next(1, 21); // [1, 20]
    }
}

void PrintMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            Console.Write($"{matrix[i, j]} \t");
        Console.WriteLine();
    }
}

int SummaDiagonal(int[,] matrix)
{
    int summa = 0;
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
        {
            if (i == j)
            {
                summa += matrix[i, j];
            }
        }
    }
    return summa;
}

Console.Clear();
Console.Write("Введите размер массива: ");
int[] size = Console.ReadLine().Split().Select(x => int.Parse(x)).ToArray();
int[,] matrix = new int[size[0], size[1]];
Console.WriteLine("Начальный массив:");
InputMatrix(matrix);
PrintMatrix(matrix);
Console.WriteLine($"Результат: {SummaDiagonal(matrix)}");
```

# Задача 52. Задайте двумерный массив из целых чисел. Найдите среднее арифметическое элементов в каждом столбце.
```
void InputMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            matrix[i, j] = new Random().Next(0, 9);
    }
}

void PrintMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            Console.Write($"{matrix[i, j]} \t");
        Console.WriteLine();
    }
}

void SummAverage(int[,] matrix, double[] array)
{
    for (int j = 0; j < matrix.GetLength(1); j++)
    {
        double summ = 0;

        for (int i = 0; i < matrix.GetLength(0); i++)
        {
            summ = summ + matrix[i, j];

        }

        array[j] = array[j] + Math.Round(summ/matrix.GetLength(0), 2);
    }
}

Console.Clear();
Console.Write("Введите размер массива: ");
int[] size = Console.ReadLine().Split().Select(x => int.Parse(x)).ToArray();
int[,] matrix = new int[size[0], size[1]];
Console.WriteLine("Двумерный массив:");
InputMatrix(matrix);
PrintMatrix(matrix);
double[] array = new double[matrix.GetLength(1)];
SummAverage(matrix, array);

Console.WriteLine($"Среднее арифметическое каждого столбца:  [{string.Join(", ", array)}]");
```

# Транспонирование. (https://acmp.ru/asp/do/index.asp?main=task&id_course=1&id_section=8&id_topic=120&id_problem=745)
## Задана целочисленная матрица, состоящая из N строк и M столбцов. Требуется транспонировать ее относительно горизонтали.
```
void InputMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            matrix[i, j] = new Random().Next(0, 100);
    }
}

void PrintMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            Console.Write($"{matrix[i, j]} \t");
        Console.WriteLine();
    }
}

void Shift(int[,] matrix,int[,] result)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
        {
            result[matrix.GetLength(0) - i - 1, j] = matrix[i, j];
        }
    }
}

Console.Clear();
Console.Write("Введите размер массива: ");
int[] size = Console.ReadLine().Split().Select(x => int.Parse(x)).ToArray();
int[,] matrix = new int[size[0], size[1]];
int[,] result = new int[size[0], size[1]];
Console.WriteLine("Двумерный массив:");
InputMatrix(matrix);
PrintMatrix(matrix);
Shift(matrix,result);
Console.WriteLine("Массив после Транспонирования:");
PrintMatrix(result);
```

# Миша и негатив. (https://acmp.ru/asp/do/index.asp?main=task&id_course=1&id_section=8&id_topic=121&id_problem=749)
## Миша уже научился хорошо фотографировать и недавно увлекся программированием. Первая программа, которую он написал, позволяет формировать негатив бинарного черно-белого изображения. Бинарное черно-белое изображение – это прямоугольник, состоящий из пикселей, каждый из которых может быть либо черным, либо белым. Негатив такого изображения получается путем замены каждого черного пикселя на белый, а каждого белого пикселя – на черный. Миша, как начинающий программист, написал свою программу с ошибкой, поэтому в результате ее исполнения мог получаться некорректный негатив. Для того чтобы оценить уровень несоответствия получаемого негатива исходному изображению, Миша начал тестировать свою программу. В качестве входных данных он использовал исходные изображения. Сформированные программой негативы он начал тщательно анализировать, каждый раз определяя число пикселей негатива, которые получены с ошибкой. Требуется написать программу, которая в качестве входных данных использует исходное бинарное черно-белое изображение и полученный Мишиной программой негатив, и на основе этого определяет количество пикселей, в которых допущена ошибка.
```
void InputMatrix(char[,] matrix)
{
    int symbol = 0;
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
        {
            symbol = new Random().Next(0, 2);
            if (symbol == 1)
                matrix[i, j] = 'W';
            else
                matrix[i, j] = 'B';
        }    
    }
}

void PrintMatrix(char[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            Console.Write($"{matrix[i, j]} \t");
        Console.WriteLine();
    }
}

int CheckPosition(char[,] matrix,char[,] result)
{
    int check = 0;
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
        {
            if(matrix[i,j] == result[i,j])
                check++;
        }
    }

    return check;
}

Console.Clear();
Console.Write("Введите размер массива: ");
int[] size = Console.ReadLine().Split().Select(x => int.Parse(x)).ToArray();
char[,] matrix = new char[size[0], size[1]];
char[,] result = new char[size[0], size[1]];
Console.WriteLine("Двумерный массив:");
InputMatrix(matrix);
PrintMatrix(matrix);
Console.WriteLine("");
InputMatrix(result);
PrintMatrix(result);

int check = CheckPosition(matrix,result);
Console.Write($"Неправильно сформированых символов: {check}");
```

# Заполнение диагональю.
```
void InputMatrix(int[,] matrix)
{
    int number = 1;
    if (matrix.GetLength(0) == matrix.GetLength(1))
    {
        for (int i = 1-matrix.GetLength(0); i <= matrix.GetLength(0)-1; i++)
        {
            for (int j = 0; j < matrix.GetLength(1); j++)
            {
                int k = j - i;
                if (k < 0 || k >= matrix.GetLength(1))
                    continue;

                matrix[j, matrix.GetLength(1)-k-1] = number++;
            }
        }
    }
    else if (matrix.GetLength(0) > matrix.GetLength(1))
    {
        int r = matrix.GetLength(0) - matrix.GetLength(1);
        for (int i = 1-matrix.GetLength(0); i <= matrix.GetLength(0)-1; i++)
        {
            for (int j = 0; j < matrix.GetLength(1) + r; j++)
            {
                int k = j - i;
                if (k < 0 || k >= matrix.GetLength(1))
                    continue;

                matrix[j, matrix.GetLength(1)-k-1] = number++;
            }
        }
    }
    else
    {
        int r = matrix.GetLength(1) - matrix.GetLength(0);
        for (int i = 1-matrix.GetLength(0); i < matrix.GetLength(0)+r; i++)
        {
            for (int j = 0; j < matrix.GetLength(1)-r; j++)
            {
                int k = j - i + r;

                if (k < 0 || k >= matrix.GetLength(1))
                    continue;

                matrix[j, matrix.GetLength(1)-k-1] = number++;
            }
        }
    }
}

void PrintMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            Console.Write($"{matrix[i, j]} \t");
        Console.WriteLine();
    }
}

Console.Clear();
Console.Write("Введите размер массива: ");
int[] size = Console.ReadLine().Split().Select(x => int.Parse(x)).ToArray();
int[,] matrix = new int[size[0], size[1]];
Console.WriteLine("Двумерный массив:");
InputMatrix(matrix);
PrintMatrix(matrix);
```

# Задача 53: Задайте двумерный массив. Напишите программу, которая поменяет местами первую и последнюю строку массива.
```
void InputMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            matrix[i, j] = new Random().Next(1, 21); // [1, 20]
    }
}

void PrintMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            Console.Write($"{matrix[i, j]} \t");
        Console.WriteLine();
    }
}

void ReplaceFirstLastRow(int[,] matrix)
{
    for (int j = 0; j < matrix.GetLength(1); j++)
    {
        int temp = matrix[0, j];
        matrix[0, j] = matrix[matrix.GetLength(0) - 1, j];
        matrix[matrix.GetLength(0) - 1, j] = temp;
    }
}

Console.Clear();
Console.Write("Введите размер массива: ");
int[] size = Console.ReadLine().Split().Select(x => int.Parse(x)).ToArray();
int[,] matrix = new int[size[0], size[1]];
Console.WriteLine("Начальный массив:");
InputMatrix(matrix);
PrintMatrix(matrix);
ReplaceFirstLastRow(matrix);
Console.WriteLine("Конечный массив:");
PrintMatrix(matrix);
```

# Задача 54: Задайте двумерный массив. Напишите программу, которая упорядочит по убыванию элементы каждой строки двумерного массива.
```
void InputMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            matrix[i, j] = new Random().Next(0, 10);
    }
}

void PrintMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            Console.Write($"{matrix[i, j]} \t");
        Console.WriteLine();
    }
}

void SortDescending(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
        {
            for (int row = j; row < matrix.GetLength(1); row++)
            {
                if (matrix[i, j] < matrix[i, row])
                {
                    int temp = matrix[i, row];
                    matrix[i, row] = matrix[i, j];
                    matrix[i, j] = temp;
                }
            }

        }
    }
}

Console.Clear();
Console.Write("Введите размер массива: ");

int[] size = Console.ReadLine().Split().Select(x => int.Parse(x)).ToArray();
int[,] matrix = new int[size[0], size[1]];
Console.WriteLine("Начальный массив:");
InputMatrix(matrix);
PrintMatrix(matrix);
SortDescending(matrix);
Console.WriteLine("Сортировка по убыванию:");
PrintMatrix(matrix);
```

# Задача 55: Задайте двумерный массив. Напишите программу, которая заменяет строки на столбцы. В случае, если это невозможно, программа должна вывести сообщение для пользователя.
```
void InputMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            matrix[i, j] = new Random().Next(1, 21); // [1, 20]
    }
}

void PrintMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            Console.Write($"{matrix[i, j]} \t");
        Console.WriteLine();
    }
}

void ReplaceFirstLastRow(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = i + 1; j < matrix.GetLength(1); j++)
        {
            int temp = matrix[i, j];
            matrix[i, j] = matrix[j, i];
            matrix[j, i] = temp;
        }
    }
}

Console.Clear();
Console.Write("Введите размер массива: ");
int[] size = Console.ReadLine().Split().Select(x => int.Parse(x)).ToArray();
while (size[0] != size[1])
{
    Console.Write("Вы ошиблись!\nВведите размер массива: ");
    size = Console.ReadLine().Split().Select(x => int.Parse(x)).ToArray();
}
int[,] matrix = new int[size[0], size[1]];
Console.WriteLine("Начальный массив:");
InputMatrix(matrix);
PrintMatrix(matrix);
ReplaceFirstLastRow(matrix);
Console.WriteLine("Конечный массив:");
PrintMatrix(matrix);
```

# Задача 56: Задайте прямоугольный двумерный массив. Напишите программу, которая будет находить строку с наименьшей суммой элементов.
```
void InputMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            matrix[i, j] = new Random().Next(0, 10);
    }
}

void PrintMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            Console.Write($"{matrix[i, j]} \t");
        Console.WriteLine();
    }
}

int SearchMinIndex(int[,] matrix)
{
    int index = 0;
    int min = 0;
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        int sum = 0;
        for (int j = 0; j < matrix.GetLength(1); j++)
        {
            if (i==0)
                min = min + matrix[i,j];
            else
                sum = sum + matrix[i,j];
        }

        if (i==0)
        {
            index = i;
        }
        else if (min>=sum)
        {
            min = sum;
            index = i;  
        }
    }

    return index;
}

Console.Clear();
Console.Write("Введите размер массива: ");

int[] size = Console.ReadLine().Split().Select(x => int.Parse(x)).ToArray();
while (size[0] != size[1])
{
    Console.Write("Вы ошиблись!\nВведите размер массива: ");
    size = Console.ReadLine().Split().Select(x => int.Parse(x)).ToArray();
}
int[,] matrix = new int[size[0], size[1]];
Console.WriteLine("Начальный массив:");
InputMatrix(matrix);
PrintMatrix(matrix);
int minIndex = SearchMinIndex(matrix);
Console.WriteLine($"Cтрока с наименьшей суммой элементов: {minIndex + 1}");
```

# Задача 57: Составить частотный словарь элементов двумерного массива. Частотный словарь содержит информацию о том, сколько раз встречается элемент входных данных.
```
bool checkElement(int[] array, int number)
{
    for (int i = 0; i < array.Length; i++)
    {
        if (array[i] == number)
            return false;
    }
    return true;
}

int inputMatrix(int[,] matrix, int[] array)
{
    int k = 0;
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
        {
            matrix[i, j] = new Random().Next(1, 11); // [1, 10]
            if (checkElement(array, matrix[i, j]))
            {
                array[k] = matrix[i, j];
                k++;
            }
            Console.Write($"{matrix[i, j]} \t");
        }
        Console.WriteLine();
    }
    return k;
}


void SwapFirstLastString (int[,] matrix, int[] array, int countArray)
{
    for (int k = 0; k < countArray; k++)
    {
        int count = 0;
        for (int i = 0; i < matrix.GetLength(0); i++)
        {
            for (int j = 0; j < matrix.GetLength(1); j++)
            {       
                if (array[k] == matrix[i, j])
                    count++;
            }
        }
        Console.WriteLine($"Элемент {array[k]} встречается {count} раз");
    }

}

Console.Clear();
Console.Write("Введите размеры матрицы: ");
int[] coord = Console.ReadLine().Split(" ").Select(x => int.Parse(x)).ToArray();
int[,] matrix = new int[coord[0], coord[1]];
int[] array = new int[coord[0] * coord[1]];
Console.WriteLine("Начальный массив: ");
int countArray = inputMatrix(matrix, array);
Console.WriteLine();
Console.WriteLine($"[{string.Join(", ", array)}]");
SwapFirstLastString(matrix, array, countArray);
```

# Задача 58: Задайте две матрицы. Напишите программу, которая будет находить произведение двух матриц.
```
void InputMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            matrix[i, j] = new Random().Next(0, 10);
    }
}

void PrintMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            Console.Write($"{matrix[i, j]} \t");
        Console.WriteLine();
    }
}

void  MultiplicationMatrix(int[,] result, int[,] matrix1, int[,] matrix2)
{
    for (int i = 0; i < result.GetLength(0); i++)
    {
        for (int j = 0; j < result.GetLength(1); j++)
        {
            result[i, j] = 0;
            for (int k = 0; k < matrix1.GetLength(1); k++)
            {
                result[i, j] += matrix1[i, k] * matrix2[k, j];
            }
        }
    }
}

Console.Clear();
Console.Write("Введите размер массива: ");

int[] size = Console.ReadLine().Split().Select(x => int.Parse(x)).ToArray();
while (size[0] != size[1])
{
    Console.Write("Вы ошиблись!\nВведите размер массива: ");
    size = Console.ReadLine().Split().Select(x => int.Parse(x)).ToArray();
}
int[,] matrix1 = new int[size[0], size[1]];
int[,] matrix2 = new int[size[0], size[1]];
int[,] result = new int[size[0], size[1]];
Console.WriteLine("Начальный массив 1: ");
InputMatrix(matrix1);
PrintMatrix(matrix1);
Console.WriteLine("Начальный массив 2: ");
InputMatrix(matrix2);
PrintMatrix(matrix2);
Console.WriteLine("Результат произведения 2-х массивов: ");
MultiplicationMatrix(result, matrix1, matrix2);
PrintMatrix(result);
```

# Задача 59. Задайте двумерный массив из целых чисел. Напишите программу, которая удалит строку и столбец, на пересечении которых расположен наименьший элемент массива.
```
void InputMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
        {
            matrix[i, j] = new Random().Next(1, 11); // [1, 10]
            Console.Write($"{matrix[i, j]} \t");
        }
        Console.WriteLine();
    }
}


void SwapFirstLastString(int[,] matrix)
{
    int minValue = matrix[0, 0], minRow = 0, minColumn = 0;
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
        {
            if (matrix[i, j] < minValue)
            {
                minValue = matrix[i, j];
                minRow = i;
                minColumn = j;
            }
        }
    }
    Console.WriteLine($"Минимум {minValue} на позиции({minRow + 1}, {minColumn + 1})");
    Console.WriteLine();
    Console.WriteLine("Конечный массив");
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        if (i != minRow)
        {
            for (int j = 0; j < matrix.GetLength(1); j++)
            {
                if (j != minColumn)
                    Console.Write($"{matrix[i, j]} \t");
            }
            Console.WriteLine();
        }
    }
}

Console.Clear();
Console.Write("Введите размер матрицы: ");
int[] coord = Console.ReadLine().Split(" ").Select(x => int.Parse(x)).ToArray();
int[,] matrix = new int[coord[0], coord[1]];
Console.WriteLine("Начальный массив");
InputMatrix(matrix);
SwapFirstLastString(matrix);
```

# Задача 60. ...Сформируйте трёхмерный массив из неповторяющихся двузначных чисел. Напишите программу, которая будет построчно выводить массив, добавляя индексы каждого элемента.
```
void InputMatrix(int[,,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
        {
            for (int k = 0; k < matrix.GetLength(2); k++)
                matrix[i, j, k] = RandomValue(matrix, i, j, k); 
        }
    }
}

static int RandomValue(int[,,] matrix, int i, int j, int k)
{
    int value = default;
    bool flag = true;
    while (flag)
    {
        bool noStop = true;
        value = new Random().Next(10, 100);
        for (int x = 0; x < matrix.GetLength(0) && noStop; x++)
        {
            for (int y = 0; y < matrix.GetLength(1) && noStop; y++)
            {
                for (int z = 0; z < matrix.GetLength(2) && noStop; z++)
                {
                    if (matrix[x, y, z] == value) 
                        noStop = false; 
                    if (x == i && y == j && z == k) 
                        flag = false; 
                }
            }
        }
    }
    return value;
}

void PrintMatrix(int[,,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
        {
            for (int k = 0; k < matrix.GetLength(2); k++) 
                Console.Write($"{matrix[i, j, k], 1}({i},{j},{k}) \t");
            Console.WriteLine();
        }
    }
}

Console.Clear();
Console.WriteLine("Массив размером 2 x 2 x 2: ");
int[,,] matrix = new int[2, 2, 2];
InputMatrix(matrix);
PrintMatrix(matrix);
```

# Задача 61: Вывести первые N строк треугольника Паскаля. Сделать вывод в виде равнобедренного треугольника.
```
const int cellWidth = 3;

private static void Main(string[] args)
{
    void FillTriangle(int[,] matrix, int row)
    {
        for (int i = 0; i < row; i++)
        {
            matrix[i, 0] = 1;
            matrix[i, i] = 1;
        }

        for (int i = 2; i < row; i++)
        {
            for (int j = 1; j <= i; j++)
            {
                matrix[i, j] = matrix[i - 1, j - 1] + matrix[i - 1, j];
            }
        }
    }

    void PrintTriangle(int[,] matrix, int row)
    {
        int col = cellWidth * row;
        for (int i = 0; i < row; i++)
        {
            for (int j = 0; j <= i; j++)
            {
                Console.SetCursorPosition(col, i + 1);
                if (matrix[i, j] != 0)
                    Console.Write($"{matrix[i, j], cellWidth}");

                col += cellWidth * 2;
            }

            col = cellWidth * row - cellWidth * (i + 1);
            Console.WriteLine();
        }
    }

    Console.Clear();
    Console.Write("Введите количество строк треугольника Паскаля: ");
    int row = Convert.ToInt32(Console.ReadLine());
    int[,] matrix = new int[row, row];

    FillTriangle(matrix, row);
    PrintTriangle(matrix, row);
}
```

# Задача 62. Напишите программу, которая заполнит спирально массив 4 на 4.
```
void PrintMatrix(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            Console.Write($"{matrix[i, j]} \t");
        Console.WriteLine();
    }
}

Console.Clear();
Console.Write("Cпиральный массив 4 на 4: ");
int[,] matrix = new int[4, 4];
Console.WriteLine(); 

int temp = 1;
int i = 0;
int j = 0;

while (temp <= matrix.GetLength(0) * matrix.GetLength(1))
{
    matrix[i, j] = temp;
    temp++;
    if (i <= j + 1 && i + j < matrix.GetLength(1) - 1)
        j++;
    else if (i < j && i + j >= matrix.GetLength(0) - 1)
        i++;
    else if (i >= j && i + j > matrix.GetLength(1) - 1)
        j--;
    else
        i--;
}

PrintMatrix(matrix);
```

# Задача 63. Задайте значение N. Напишите программу, которая выведет все натуральные числа в промежутке от 1 до N.
```
string OutputNumbers(int n)
{
    if (n == 1)
        return "1";
    return $"{n}, " + OutputNumbers(n - 1);
}


Console.Clear();
Console.Write("Введите число: ");
int n = Convert.ToInt32(Console.ReadLine());
Console.WriteLine(OutputNumbers(n));
```

# Задача 64. Задайте значение N. Напишите программу, которая выведет все натуральные числа в промежутке от N до 1. Выполнить с помощью рекурсии.
```
int ReadData(string line)
{
    Console.Write(line);
    int number = int.Parse(Console.ReadLine() ?? "0");
    return number;
}

// Печать результата
void PrintResult(string prefix)
{
    Console.WriteLine(prefix);
}

// Функция рекурсии

string LineGenRec(int num)
{
    if (num == 0)
    {
        return string.Empty;
    }
    else
    {
        //return LineGenRec(num - 1) + " " + num ;
        return num + " " + LineGenRec (num - 1);
    }
}

int number = ReadData("Введите число N: ");
string resultLine = LineGenRec(number);
PrintResult(resultLine);
```

# Задача 65. Задайте значения M и N. Напишите программу, которая выведет все натуральные числа в промежутке от M до N.
```
string OutputNumbers(int m, int n)
{
    if (n == m)
        return $"{m}";
    return OutputNumbers(m, n - 1) + $", {n}";
}


Console.Clear();
Console.Write("Введите 1-ое число: ");
int m = Convert.ToInt32(Console.ReadLine());
Console.Write("Введите 2-ое число: ");
int n = Convert.ToInt32(Console.ReadLine());
Console.WriteLine(OutputNumbers(m, n));
```

# Задача 66. Задайте значения M и N. Напишите программу, которая найдёт сумму натуральных элементов в промежутке от M до N.
```
int sum(int m, int n)
{ 
    if (m == n)
        return m;
    return sum(m, n - 1) + n;
}

Console.Clear();
Console.Write("Введите число M: ");
int m = Convert.ToInt32(Console.ReadLine());
Console.Write("Введите число N: ");
int n = Convert.ToInt32(Console.ReadLine());
while (m > n)
{
    Console.Write("Вы ошиблись!\nВведите число N больше числа M: ");
    n = Convert.ToInt32(Console.ReadLine());
}

Console.WriteLine($"M = {m}; N = {n} -> {sum(m, n)}");
```

# Задача 67. Напишите программу, которая будет принимать на вход число и возвращать сумму его цифр.
```
int SummaCifr(int n)
{
    if (n < 10 || n % 10 == n || n / 10 == 0)
        return n;
    return SummaCifr(n / 10) + n % 10;
}


Console.Clear();
Console.Write("Введите число: ");
int n = Convert.ToInt32(Console.ReadLine());
Console.WriteLine(SummaCifr(n));
```

# Задача 68. Напишите программу вычисления функции Аккермана с помощью рекурсии. Даны два неотрицательных числа m и n.
```
int Ackerman(int m, int n)
{ 
    if (m == 0) 
        return n + 1;
    else if (n == 0) 
        return Ackerman(m - 1, 1);
    else 
        return Ackerman(m - 1, Ackerman(m, n - 1));
}

Console.Clear();
Console.Write("Введите число M: ");
int m = Convert.ToInt32(Console.ReadLine());
while (m < 0)
{
    Console.Write("Вы ошиблись!\nВведите неотрицательное число M: ");
    m = Convert.ToInt32(Console.ReadLine());
}
Console.Write("Введите число N: ");
int n = Convert.ToInt32(Console.ReadLine());
while (n < 0)
{
    Console.Write("Вы ошиблись!\nВведите неотрицательное число N: ");
    n = Convert.ToInt32(Console.ReadLine());
}

Console.WriteLine($"M = {m}; N = {n} -> A(m,n) = {Ackerman(m, n)}");
```

# Задача 69. Напишите программу, которая на вход принимает два числа A и B, и возводит число А в целую степень B с помощью рекурсии.
```
int PowRec(int a, int b)
{
    if (b == 0)
        return 1;
    return PowRec(a, b - 1) * a;
}


Console.Clear();
Console.Write("Введите число: ");
int a = Convert.ToInt32(Console.ReadLine());
Console.Write("Введите степень: ");
int b = Convert.ToInt32(Console.ReadLine());
Console.WriteLine(PowRec(a, b));
```
