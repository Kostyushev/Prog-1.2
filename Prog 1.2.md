using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApplication1_1
{
    class Program
    {
        static void Main(String[] args)
        {
            Console.Write("Введите x: ");
            Single x = Convert.ToSingle(Console.ReadLine());
            Console.Write("Введите y: ");
            Single y = Convert.ToSingle(Console.ReadLine());
            String insector = "Точка лежит в плоскости.";
            String outofsector = "Точка не лежит в плоскости.";
            //I Четверть
            if (x > 0 & y > 0)
            {
                Console.WriteLine(outofsector);
            }
            //II Четверть
            if (x <= 0 && y >= 0)
            {
                if (x <= -0.5)
                {
                    if (y <= 1)
                    {
                        Console.WriteLine(insector);
                    }
                    else
                    {
                        Console.WriteLine(outofsector);
                    }
                }
                else
                {
                    if (y >= 0.5)
                    {
                        if (x >= -1)
                        {
                            Console.WriteLine(insector);
                        }
                        else
                        {
                            Console.WriteLine(outofsector);
                        }
                    }
                }
                if (x > -0.5 & y < 0.5)
                {
                    Console.WriteLine(outofsector);
                }
            }
            //III Четверть
            if (x < 0 & y < 0)
            {
                Console.WriteLine(outofsector);
            }
            //IV Четверть
            if (x >= 0 & y <= 0)
            {
                if (Math.Sqrt((x * x) + (y * y)) <= 1)
                {
                    Console.WriteLine(insector);
                }
                else
                {
                    Console.WriteLine(outofsector);
                }
            }
            Console.ReadLine();
        }

      }
    }
