# add

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using NUnit.Framework;
using Triangle;

using System.Threading.Tasks;

namespace ClassLibrary1
{
    public class Class1
    {

        [TestFixture]

        public class Triangle
        {
            [Test]

            public void InputSides_4_4_4_Expected_FormsEquilateral()
            {
                //Arrange
                int trs1 = 4;
                int trs2 = 4;
                int trs3 = 4;
                string expected = "Forms Equilateral";

                //Act
                string actual = TriangleSolver.Analyze(trs1, trs2, trs3);

                //Assert

                Assert.AreEqual(expected, actual);



            }

            [Test]

            public void InputSides_40_50_60_Expected_FormsScalene()
            {
                //Arrange
                int trs1 = 40;
                int trs2 = 50;
                int trs3 = 60;
                string expected = "Forms Scalene";

                //Act
                string actual = TriangleSolver.Analyze(trs1, trs2, trs3);

                //Assert

                Assert.AreEqual(expected, actual);



            }


            [Test]

            public void InputSides_40_40_40_Expected_FormsEquilateral()
            {
                //Arrange
                int trs1 = 40;
                int trs2 = 40;
                int trs3 = 40;
                string expected = "Forms Equilateral";

                //Act
                string actual = TriangleSolver.Analyze(trs1, trs2, trs3);

                //Assert

                Assert.AreEqual(expected, actual);


            }
            [Test]

            public void InputSides_0_0_0_Expected_Formstrianglecannotbecreated()
            {
                //Arrange
                int trs1 = 0;
                int trs2 = 0;
                int trs3 = 0;
                string expected = "triangle cannot be created";

                //Act
                string actual = TriangleSolver.Analyze(trs1, trs2, trs3);


                //Assert

                Assert.AreEqual(expected, actual);

            }



        }
    }
}
