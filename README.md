using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Triangle
{
    public static class TriangleSolver
    {
         public static string Analyze(int side1, int side2, int side3)
        {
            string answer = string .Empty ;


            if (side1 + side2 > side3 || side2 + side3 > side1 || side1 + side3 > side2)
            {

                if ((side1 == side2) && (side1 == side3))
                {
                    answer = ("Forms Equilateral");

                }
                else if ((side1 == side2) || (side2 == side3) || (side1 == side3))
                {
                    answer = ("Forms Isosceles");
                   

                }
                else
                {
                    answer = ("Forms Scalene");

                }

            }
            else
            {
                answer=("triangle cannot be created");
            }
            return answer;


        }

        
    }
}











