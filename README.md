# Prosjek
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace UvodniProjekt3d
{
    internal class Program
    {
        static void Main(string[] args)
        {
  
            Console.WriteLine("######################");
            Console.WriteLine("Izračunavanje prosjeka");
            Console.WriteLine("######################");
            Console.WriteLine("Za kraj unesite nulu.");

            int ocjena, zbrojOcjena = 0;
            double prosjek=0, brojPredmeta = 0.00;

            do 
                {
             
                Console.WriteLine("Unesi ocjenu: "); 
                ocjena = Convert.ToInt32(Console.ReadLine());

                if (ocjena <= 5 && ocjena > 1)
                {
                    zbrojOcjena = zbrojOcjena + ocjena;

                    brojPredmeta++;

                    prosjek = zbrojOcjena / brojPredmeta;
                }
                else if(ocjena ==1){
                    prosjek = 1;
                    break;
                }
                else
                {
                    Console.WriteLine("Upišite ispravnu ocjenu.");
                }                                    
                   
                }
            while (ocjena != 0);
            

            Console.WriteLine("Prosjek ocjena je: "+ prosjek);

            Console.ReadKey();
        }
    }
}
