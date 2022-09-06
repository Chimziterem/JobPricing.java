# JobPricing.java
import java.util.Scanner;
class JobPricing {
    public static void main(String[] args) {
        String description;
        double materials;
        double hoursOnJob;
        double hoursTraveling;
        double price;
        Scanner input = new Scanner(System.in);
        System.out.print("Enter job description >> ");
        description = input.nextLine();
        System.out.print("Enter cost of materials >> ");
        materials = input.nextDouble();
        System.out.print("Enter hours on the job work >> ");
        hoursOnJob = input.nextDouble();
        System.out.print("Enter hours traveling >> ");
        hoursTraveling = input.nextDouble();
        price = computePrice(materials, hoursOnJob, hoursTraveling);
        System.out.println("The price for " + description +
                           " is $" + price);
    }

    public static double computePrice(double materials, double hours, double travel) {
         final double HOURLY_WAGE_PER_HOUR = 35.0;
        final double TRAVEL_PRICE_PER_HOUR = 12.0;

        double WageCost = hours * HOURLY_WAGE_PER_HOUR;
        double TravelCost = travel * TRAVEL_PRICE_PER_HOUR;
        double TotalPrice = materials + WageCost + TravelCost;

        return(TotalPrice);
    
    }
}
