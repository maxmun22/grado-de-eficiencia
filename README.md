import java.util.Scanner;

public class EvaluadorEficiencia {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Información del alumno
        System.out.print("Nombre del alumno: ");
        String nombreAlumno = scanner.nextLine();

        // Entradas
        System.out.print("Ingrese el número de tornillos defectuosos: ");
        int defectuosos = scanner.nextInt();

        System.out.print("Ingrese el número total de tornillos producidos: ");
        int producidos = scanner.nextInt();

        // Evaluación de eficiencia
        int grado = determinarGrado(defectuosos, producidos);

        // Resultado
        System.out.println("\n--- Resultado de Evaluación ---");
        System.out.println("Alumno: " + nombreAlumno);
        System.out.println("Tornillos defectuosos: " + defectuosos);
        System.out.println("Tornillos producidos: " + producidos);
        System.out.println("Grado de eficiencia: " + grado);
    }

    public static int determinarGrado(int defectuosos, int producidos) {
        boolean cumpleCondicion1 = defectuosos < 200;
        boolean cumpleCondicion2 = producidos > 10000;

        if (cumpleCondicion1 && cumpleCondicion2) {
            return 8;
        } else if (cumpleCondicion1) {
            return 6;
        } else if (cumpleCondicion2) {
            return 7;
        } else {
            return 5;
        }
    }
}
