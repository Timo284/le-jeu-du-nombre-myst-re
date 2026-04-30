import java.util.Random;
import java.util.Scanner;

public class JeuNombre {

    public static void jeuNombre() {
        Random random = new Random();
        int nombreSecret = random.nextInt(100) + 1;
        int essais = 0;
        Scanner scanner = new Scanner(System.in);

        System.out.println("Bienvenue ! J'ai choisi un nombre entre 1 et 100.");

        while (true) {
            System.out.print("Entrez un nombre : ");
            int choix = scanner.nextInt();
            essais++;

            if (choix < nombreSecret) {
                System.out.println("Trop petit !");
            } else if (choix > nombreSecret) {
                System.out.println("Trop grand !");
            } else {
                System.out.println("Bravo ! Vous avez trouvé en " + essais + " essai(s) !");
                break;
            }
        }

        scanner.close();
    }

    public static void main(String[] args) {
        jeuNombre();
    }
}
