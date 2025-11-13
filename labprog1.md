import java.util.Scanner;

public class QuadraticEquation {
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);

        System.out.print("Enter a, b, c: ");
        double a = s.nextDouble();
        double b = s.nextDouble();
        double c = s.nextDouble();

        if (a == 0) {
            System.out.println("Not a quadratic equation.");
        } else {
            double d = b * b - 4 * a * c;

            if (d > 0) {
                double r1 = (-b + Math.sqrt(d)) / (2 * a);
                double r2 = (-b - Math.sqrt(d)) / (2 * a);
                System.out.println("Roots are real and different:");
                System.out.println(r1 + " and " + r2);
            } else if (d == 0) {
                double r = -b / (2 * a);
                System.out.println("Roots are real and equal:");
                System.out.println(r);
            } else {
                System.out.println("Roots are complex (not real).");
            }
        }
    }
}
