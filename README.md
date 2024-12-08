# Multiplication-of-Array
public class ArrayMultiplication {
    public ArrayMultiplication() {
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the no. of rows");
        int n = sc.nextInt();
        System.out.println("Enter the no. of columns:");
        int m = sc.nextInt();
        int[][] arr1 = new int[n][m];
        int[][] arr2 = new int[n][m];
        int[][] ans = new int[n][m];
        System.out.println("Enter the elements in First Matrix: ");

        int i;
        int j;
        for(i = 0; i < n; ++i) {
            for(j = 0; j < m; ++j) {
                arr1[i][j] = sc.nextInt();
            }
        }

        System.out.println("Enter the elements of Second Matrix: ");

        for(i = 0; i < n; ++i) {
            for(j = 0; j < m; ++j) {
                arr2[i][j] = sc.nextInt();
            }
        }

        System.out.println("The multiplication of these two array is :");

        for(i = 0; i < n; ++i) {
            for(j = 0; j < m; ++j) {
                ans[i][j] = 0;

                for(int k = 0; k < n; ++k) {
                    ans[i][j] += arr1[i][k] * arr2[k][j];
                }
            }
        }

        for(i = 0; i < n; ++i) {
            for(j = 0; j < m; ++j) {
                System.out.print(ans[i][j] + " ");
            }

            System.out.println();
        }

    }
}
