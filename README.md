# Photo-Gallery
Just another repository
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Photo_Gallery
{
    class Program
    {
        static void Main(string[] args)
        {
            int num = int.Parse(Console.ReadLine());
            int day = int.Parse(Console.ReadLine());
            int month = int.Parse(Console.ReadLine());
            int year = int.Parse(Console.ReadLine());
            int hours = int.Parse(Console.ReadLine());
            int minutes = int.Parse(Console.ReadLine());
            double size = int.Parse(Console.ReadLine());
            int width = int.Parse(Console.ReadLine());
            int leight = int.Parse(Console.ReadLine());

            Console.WriteLine($"Name: DSC_{num:d4}.jpg");
            Console.WriteLine($"Date Taken: {day:d2}/{month:d2}/{year:d4} {hours:d2}:{minutes:d2}");

            if (size < 1000)
            {
                Console.WriteLine($"Size: {size}B");
            }
            else if (size < 1000000)
            {
                size /= 1000;
                Console.WriteLine($"Size: {size}KB");
            }
            else
            {
                size /= 1000000.00;
                Console.WriteLine($"Size: {size}MB");
            }

            if (width > leight)
            {
                Console.WriteLine($"Resolution: {width}x{leight} (landscape)");
            }
            else if (width < leight)
            {
                Console.WriteLine($"Resolution: {width}x{leight} (portrait)");
            }
            else
            {
                Console.WriteLine($"Resolution: {leight}x{leight} (square)");
            }
        }
    }
}
