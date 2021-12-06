using System;
 
class GFG
{
    public static char[] encryptStr(String str,
                                    int n)
    {
        char[] arr = str.ToCharArray();
        String enc='null';
        for (int i = 0; i < n; i++)
        {
            if (arr[i]=='A'||arr[i]=='a')
            {
                enc=enc+"12";
            }
            else if (arr[i]=='C'||arr[i]=='c')
            {
                enc=enc+"32";
            }
            else if (arr[i]=='F'||arr[i]=='f')
            {
                enc=enc+"22";
            }
            else if (arr[i]==' ')
            {
                enc=enc+"00";
            }
            else
            {
                enc=enc+"999";
            }
        }
        return enc;
    }
    public static void Main(String[] args)
    {
        String s = Console.ReadLine();
        int n = s.Length;
        //int x = 3;
        Console.WriteLine(encryptStr(s, n));
    }
}
