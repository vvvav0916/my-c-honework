using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace ConsoleApplication6
{
    class Count
    {
        protected int a;
        protected int b;
        protected char c;
        public int A
        {
            get { return a; }
            set { a = value; }
        }
       public int B
        {
            get { return b; }
            set { b = value; }
        }
        public Char C
        {
            get { return c; }
            set { c = value; }
        }
        public void Jisuan()
        {
            a = Convert.ToInt16(Console.ReadLine());
            c = Convert.ToChar(Console.ReadLine());
            b = Convert.ToInt16(Console.ReadLine());
        }
        public double Counter()
        {
            if (c == '+') return (a + b);
            else if (c == '-') return (a - b);
            else if (c == '*') return (a * b);
            else if (c == '/') return (a / b);
            else return -1;
        }
        public void Change()
        { 
                String number1;
                String number2;
                String number3;
                number1 = Convert.ToString(a);
                number2 = Convert.ToString(b);
                if (c == '+')
                {
                    number3 = number1 + number2;
                    Console.WriteLine(number3);
                }
                else if (c == '-')
                {
                    number3 = number1.Replace(number2, "");
                    Console.WriteLine(number3);
                }
        }
        public bool Equals(int a, int b)
        {
            if (a == b) return true;
            else return false;
        }                                                                                                  

    }
}
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace ConsoleApplication6
{
    class Program
    {
        static void Main(string[] args)
        {
            Count c = new Count();
            c.Jisuan();
            c.Change();
            Console.WriteLine(c.Counter());
            if (c.Equals(c.A, c.B))
                Console.WriteLine("两数相等");
            else
                Console.WriteLine("两数不相等");
            Console.ReadKey();
        }
    }
}
