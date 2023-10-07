import java.util.Scanner;

public class currencyConverter{
    public static void main(String[] args){

        //Defining exchange rates
        
        double USDtoRand = 19.30;
        double USDtoEuro = 0.94;
        double USDtoGBP = 0.82;
        double USDtoJPY = 149.32;
        
        //Starting scanner for user input
        Scanner scanner = new Scanner( System.in);

        //Request user input
        System.out.print("Enter the amount in USD:");

        double USDamount = scanner.nextDouble();

        //Request target currency 
        System.out.println("Select the target currency: ");
        System.out.println("1. Rand");
        System.out.println("2. Euro");
        System.out.println("3. British Pound (GBP)");
        System.out.println("4. Japanese Yan (JPY)");
        System.out.println("Enter number: ");

        int num = scanner.nextInt();

        //Currency conversion
        double convertedAmount = 0.0;
        String targetCurrency = "";

        switch (num) {
            case 1: 
            convertedAmount = USDamount * USDtoRand;
            targetCurrency = "Rand";
            break;

            case 2: 
            convertedAmount = USDamount * USDtoEuro;
            targetCurrency = "Euro";
            break;

            case 3: 
            convertedAmount = USDamount * USDtoGBP;
            targetCurrency = "British Pound (GBP)";
            break;

            case 4: 
            convertedAmount = USDamount * USDtoJPY;
            targetCurrency = "Japanese Yen (JPY)";
            break;

            default:
                System.out.println("Invalid input");

        }

    //Conversion result
    System.out.println(USDamount + " USD is equal to " + convertedAmount + " " + targetCurrency);

    //Closing scanner
    scanner.close();

    }
}
****
