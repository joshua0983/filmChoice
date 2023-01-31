import java.util.*;

public class filmChoice {

    public static void main(String[] args) {
        Map<String, Integer> filmWithRating = new HashMap<String, Integer>();
        Map<String, Integer> filmWithLength = new HashMap<String, Integer>();

        Scanner in = new Scanner(System.in);
        System.out.println("Welcome! \n Enter 1 if you want to add a film.");
        int starter = in.nextInt();

        while (starter == 1) {
            Scanner filmInput = new Scanner(System.in);
            System.out.println("Enter the name of the film: \n");
            String filmName = filmInput.nextLine();

            Scanner lengthInput = new Scanner(System.in);
            System.out.println("Enter the length of the movie");
            int filmLength = in.nextInt();

            Scanner ratingInput = new Scanner(System.in);
            System.out.println("Enter your rating for this film");
            int newRating = in.nextInt();

            filmWithRating.put(filmName, newRating);
            filmWithLength.put(filmName, filmLength);

            Scanner addAnother = new Scanner(System.in);
            System.out.println("If you want to add another enter 1 \n If you want the result enter 2 \n");
            int newStarter = in.nextInt();

            if (newStarter == 2){break;
            }
            if (newStarter == 1){continue;}

        }

        LinkedHashMap<String, Integer> sortedFilmWithRating = new LinkedHashMap<String, Integer>();
        LinkedHashMap<String, Integer> sortedFilmWithLength = new LinkedHashMap<String, Integer>();

        filmWithRating.entrySet()
                .stream()
                .sorted(Map.Entry.comparingByValue(Comparator.reverseOrder()))
                .forEachOrdered(x -> sortedFilmWithRating.put(x.getKey(), x.getValue()));

        filmWithLength.entrySet()
                .stream()
                .sorted(Map.Entry.comparingByValue(Comparator.reverseOrder()))
                .forEachOrdered(x -> sortedFilmWithLength.put(x.getKey(), x.getValue()));

        System.out.println("Based on your rating, you should watch these shows accordingly: \n" + sortedFilmWithRating);
        System.out.println("Based on how long you want the movie you last, you should watch these shoes accordingly: \n" + sortedFilmWithLength);
    }
}
