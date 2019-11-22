using System; 
using System.Collections.Generic; 
using System.Linq; 
using System.Text; 
using System.Threading.Tasks; 


namespace krychemass
{
    class Program
    {
        static void Main(string[] args)
        {
            Random rnd = new Random();


            int Mono = 0;
            Console.Write("Введите размер массива: ");
            int number_N = int.Parse(Console.ReadLine());
            int[] mass = new int[number_N];
            for (int i = 0; i < number_N; i++)
            {
                mass[i] = rnd.Next(100);

                Console.WriteLine(mass[i]);
            }

            for (int i = 0; i < number_N; i++)
            {

                if (i > 1)
                    if (mass[i] >= mass[i - 1])
                    {
                        Mono++;
                        Console.WriteLine($"Номер {Mono} элемента:{i}");
                    }

            }
            Console.Write("Количество элементов,больших своего левого соседа: ");
            Console.Write(Mono);
            Console.ReadKey();
        }



    }
}
