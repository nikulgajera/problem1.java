//# problem1.java
//java 
import java.util.Scanner;

public class Calculator {

    private double a;
    private double b;
    private String operation;

    public Calculator(double a, double b, String operation) {
        this.a = a;
        this.b = b;
        this.operation = operation;
    }

    public double add() {
        return a + b;
    }

    public double subtract() {
        return a - b;
    }

    public double multiply() {
        return a * b;
    }

    public double divide() {
        return a / b;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Enter first number: ");
        double a = scanner.nextDouble();

        System.out.println("Enter second number: ");
        double b = scanner.nextDouble();

        System.out.println("Enter operation: ");
        String operation = scanner.next();

        Calculator calculator = new Calculator(a, b, operation);

        switch (operation) {
            case "add":
                System.out.println(a + " + " + b + " = " + calculator.add());
                break;
            case "subtract":
                System.out.println(a + " - " + b + " = " + calculator.subtract());
                break;
            case "multiply":
                System.out.println(a + " * " + b + " = " + calculator.multiply());
                break;
            case "divide":
                System.out.println(a + " / " + b + " = " + calculator.divide());
                break;
            default:
                System.out.println("Invalid operation!");
        }
    }
}
