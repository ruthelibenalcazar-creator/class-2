# class-2
public class VerticalDigits {

    public static void writeVertical(int n) {
        // Opcional: manejar negativos
        if (n < 0) {
            System.out.println("-");
            n = -n;
        }

        // Caso especial para 0 (porque 0/10 = 0 y podría confundir si no se maneja)
        if (n == 0) {
            System.out.println(0);
            return;
        }

        writeVerticalHelper(n);
    }

    private static void writeVerticalHelper(int n) {
        // Caso base: un solo dígito
        if (n < 10) {
            System.out.println(n);
            return;
        }

        // Caso recursivo: imprime primero la parte izquierda
        writeVerticalHelper(n / 10);

        // Luego imprime el último dígito
        System.out.println(n % 10);
    }

    public static void main(String[] args) {
        writeVertical(1234);
        // Output:
        // 1
        // 2
        // 3
        // 4
    }
}

