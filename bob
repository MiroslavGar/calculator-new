import java.util.Scanner;

public class main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Введите математическое выражение ");
        String input = scanner.nextLine();

        try {
            int result = calculate(input);
            System.out.println(result);
        } catch (Exception e) {
            System.out.println("throws Exception // " + e.getMessage());
        }


    }

    private static int calculate(String input) throws Exception {
        String[] parts = input.split(" ");


        if (parts.length != 3) {
            throw new Exception("т.к. формат математической операции не удовлетворяет заданию - два операнда и один оператор (+, -, /, *)");
        }


        int a = Integer.parseInt(parts[0]);
        String operator = parts[1];
        int b = Integer.parseInt(parts[2]);


        if (a < 1 || a > 10 || b < 1 || b > 10) {
            throw new Exception("т.к. числа должны быть от 1 до 10 включительно");
        }

        return switch (operator) {
            case "+" -> a+b;
            case "-" -> a-b;
            case "*" -> a*b;
            case "/" -> {
                if (b == 0) {throw new Exception("деление на ноль невозможно");}
                yield a/b;
            }
            default -> throw new Exception("т.к. строка не является математической операцией");
        };
    }
}
