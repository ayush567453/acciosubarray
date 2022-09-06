# acciosubarray
import java.util.*;
import java.lang.*;
import java.io.*;

public class Main
{
	public static void main (String[] args) throws java.lang.Exception
	{
		Scanner sc = new Scanner(System.in);
        int t = sc.nextInt();
        while (t-- > 0) {
            int n = sc.nextInt();
            int arr[] = new int[n];
            for (int i = 0; i < n; i++) {
                arr[i] = sc.nextInt();
            }
            if (n <= 2) {
                System.out.println(0);
                // continue;
            }
          else{
            int ans = 0;
            int diff = arr[1] - arr[0];
            int count = 1;
            for (int i = 2; i < n; i++) {
                if (arr[i] - arr[i - 1] == diff) {
                    count++;
                } else {
                    diff = arr[i] - arr[i - 1];
                    count = 1;
                }
                ans += (count - 1);
            }
            System.out.println(ans);
          }
 
        }
    }
}
