import java.util.ArrayList;
import java.util.Scanner;

class SubsetSum {

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		int t = sc.nextInt();
		sc.nextLine();
		ArrayList<String> res = new ArrayList<String>();
		for (int k = 0; k < t; k++) {
			int n = sc.nextInt();
			ArrayList<Integer> a = new ArrayList<Integer>();
			int i = 0;

			for (i = 0; i < n; i++) {
				a.add(sc.nextInt());
			}
			sc.nextLine();
			int x = sc.nextInt();

			if (isSubsetSum(a, n, x) == true)
				res.add("YES");
			else
				res.add("NO");
		}
		for (int i = 0; i < res.size(); i++)
			System.out.println(res.get(i));

	}

	static boolean isSubsetSum(ArrayList<Integer> a, int n, int sum) {
		if (sum == 0)
			return true;
		if (n == 0 && sum != 0)
			return false;

		if (a.get(n - 1) > sum)
			return isSubsetSum(a, n - 1, sum);
		return isSubsetSum(a, n - 1, sum) || isSubsetSum(a, n - 1, sum - a.get(n - 1));
	}
}
