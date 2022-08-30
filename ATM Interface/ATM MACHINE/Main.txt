import java.util.Scanner;

public class Main{


    public static void main(String[] args){
         Account account=new Account();
        Scanner scanner = new Scanner(System.in);
        System.out.println("\nWelcome to ATM Machine,First Please create your account");
        System.out.println("\nEnter Your Full Name");
        String Name= scanner.nextLine();

        account.setpin();

        System.out.println("\nYour Initial Balance is 0.0");
        boolean quit = false;

        System.out.println("\nChoose Action\n");

        printActions();
        while (!quit) {

            int action = scanner.nextInt();
            switch (action) {
                case 1:
                    account.AddAmount();
                    break;

                case 2:
                    account.Withdrawl();
                    break;

                case 3:
                    account.CheckBalance();
                    break;

                case 4:
                    account.ChangePin();
                    break;

                case 5:
                    account.Transation();
                    break;
                case 6:
                    Quit();
                    break;

            }
            System.out.println("\nEnter your Action(1-ADD, 2-WITHDRAW, 3-BALANCE, 4-CHANGE PIN, 5-MINI STATEMENT, 6-QUIT)");
        }
    }
    public static void printActions(){
        System.out.println("                      Welcome to ATM Machine\n\n" +
                           "1.ADD MONEY                                        2.WITHDRAW \n\n"+
                           "3.BALANCE ENQUIRY                                  4.CHANGE PIN\n\n"+
                           "5.MINI STATEMENT                                   6. QUIT\n");
    }
    public static void Quit(){
        System.out.println("\nThank you for using ATM machine :)");
        System.exit(0);
    }

}