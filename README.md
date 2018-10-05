programa 1
(Main) 
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp10
{
    class Program
    {
        static void Main(string[] args)
        {
            Class1 figura1 = new Class1();
            Random NumeroRandom = new Random();

            int n;
            Console.Write("Tamaño del Vector es  ");
            n = int.Parse(Console.ReadLine());
            Console.WriteLine("        ");
            int[] Vector = new int[n];
            for (int f = 0; f < n; f++)
            {
                Vector[f] = NumeroRandom.Next(0, 100);
                Console.Write(" ");
                Console.Write(Vector[f]);
            }
            Console.WriteLine(" ");
            Console.WriteLine("---------------------------");
            Console.WriteLine("Numero Mayor es  " + figura1.mayor(Vector, n - 1, Vector[0]));
            Console.ReadKey();
        }
    }
}

Clase:
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp10
{
    class Class1
    {
        
            public int mayor(int[] x, int n, int M)
            {
                if (n == 0)
                {
                    if (M < x[n])
                    {
                        return x[0];
                    }
                    else
                    {
                        return M;
                    }
                }
                else
                {
                    if (M < x[n])
                    {
                        return mayor(x, n - 1, x[n]);
                    }
                    else
                    {
                        return mayor(x, n - 1, M);
                    }
                }
            }
        }

    }


programa 2
(Main) 
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp11
{
    class Program
    {
        static void Main(string[] args)
        {
            Class1 figura1 = new Class1();
            Random NumeroRandom = new Random();

            int x;
            Console.Write("vamaño del vector es  ");
            x = int.Parse(Console.ReadLine());
            Console.WriteLine("         ");
            int[] vector = new int[x];
            for (int f = 0; f < x; f++)
            {
                vector[f] = NumeroRandom.Next(0, 100);
                Console.Write("   ");
                Console.Write(vector[f]);
            }
            Console.WriteLine(" ");
            Console.WriteLine("        ");
            Console.WriteLine("numero menor es  " + figura1.menor(vector, x - 1,
           vector[0]));
            Console.ReadKey();
        }
    }
}
Clase:
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp11
{
    class Class1
    {
        public int menor(int[] x, int n, int menor1)
        {
            if (n == 0)
            {
                if (menor1 > x[n])
                {
                    return x[0];
                }
                else
                {
                    return menor1;
                }
            }
            else
            {
                if (menor1 > x[n])
                {
                    return menor(x, n - 1, x[n]);
                }
                else
                {
                    return menor(x, n - 1, menor1);
                }
            }
        }
    }


}

Programa 3:
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp12
{
    class Program
    {
        public static int Invertir(int x)
        {
            if (x < 10)
            {
                return x;
            }
            else
            {
                return (x % 10) * 10 + Invertir(x / 10);
            }
        }

        static void Main(string[] args)
        {
            {
                int x = 0;
                try
                {
                    Console.WriteLine("ingrese numero: ");
                    x = int.Parse(Console.ReadLine());
                    Console.WriteLine("------------------------");
                    Console.WriteLine("numero es  " + Invertir(x));
                }
                catch
                {
                    Console.WriteLine("Ingrese lo que se te pide, vuelve a intentarlo");
                }
                Console.ReadKey();
            }
        }
    }
