# Identity-Matrix-Java_interview_practice
Java program to check whether the given 2-d array is identical or not
package identity_matrix;

/**
 *
 * @author Dinesh Nanda
 */
public class IdentityMatrix {

    public static void main(String[] args) {

        int a[][] = {{1, 0, 0}, {0, 1, 0}, {0, 0, 1}};

        int count_one = 0;
        int check_zero = 0;

        for (int i = 0; i < a.length; i++) {
            for (int j = 0; j < a.length; j++) {

                if (i == j) {
                    if (a[i][j] == 1) {
                        count_one++;
                    }
                } else if (a[i][j] != 0) {
                    check_zero++;
                }
            }
        }
        if (count_one == a.length && check_zero == 0) {
            System.out.println("Identity Matrix");
        } else {
            System.out.println("Not an Identity Matrix");
        }
    }

}
