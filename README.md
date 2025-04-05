# ap-ssignment-3rd -: Write a Java program to create an abstract class GeometricShape with abstract methods area() and perimeter(). Create subclasses Triangle and Square that extend the GeometricShape class and implement the respective methods to calculate the area and perimeter of each shape. 


abstract class GeometricShape {
    abstract double area();
    abstract double perimeter();
}
class Triangle extends GeometricShape {
    double a, b, c;
    double height, base;

    Triangle(double a, double b, double c, double base, double height) {
        this.a = a;
        this.b = b;
        this.c = c;
        this.base = base;
        this.height = height;
    }

    @Override
    double area() {
        return 0.5 * base * height;
    }

    @Override
    double perimeter() {
        return a + b + c;
    }
}
class Square extends GeometricShape {
    double side;

    Square(double side) {
        this.side = side;
    }

    @Override
    double area() {
        return side * side;
    }

    @Override
    double perimeter() {
        return 4 * side;
    }
}
public class Main {
    public static void main(String[] args) {
        GeometricShape triangle = new Triangle(3, 4, 5, 3, 4);
        GeometricShape square = new Square(5);

        System.out.println("Triangle Area: " + triangle.area());
        System.out.println("Triangle Perimeter: " + triangle.perimeter());

        System.out.println("Square Area: " + square.area());
        System.out.println("Square Perimeter: " + square.perimeter());
    }
}
