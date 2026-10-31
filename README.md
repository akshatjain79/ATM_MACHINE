# ATM_MACHINE

import java.util.Scanner;
import javax.swing.text.BadLocationException;

public class ATMmachine {
    class ATM {

        float Balance;

          int PIN;

    public void checkpoint(){
        System.out.println("Enter Your pin :");
        Scanner sc =new Scanner(System.in);
        int enterdpin=sc.nextInt();
        if(enterdpin==PIN){
            menu();
        }
        else{
            System.out.println("Enter a valide PIN");


        }
        }
    }
    public void menu(){
        System.out.println("enter your choice: ");
        System.out.println("1. check A/C balance");
        System.out.println("2. Withdrow Money: ");
        System.out.println("3. Deposite Money: ");
        System.out.println("4. EXIT ");
        
        Scanner sc=new Scanner(System.in);
        int opt=sc.nextInt();
        if(opt==1){
            checkBalance();
        }
        else if(opt==2){
            WthdrowMoney();
        }
        else if(opt==3){
            depositeMoney();
        }
        else if(opt==4){
            break:
        }
        else{
            System.out.println("Plese Enter A Valide Choice");
        }

    }
    public void checkBalance(){
        System.out.println("Balance" + Balance);
        menu();
    }

        public void withdrowMoney(){
            System.out.println("Enter Amount To Withdrow");
            Scanner sc = new Scanner(System.in);
            float amount=sc.nextFloat();
            if(amount>Balance){
                System.out.println("Insufficant Balance");
            }
            else{
                Balance=Balance-amount;
                System.out.println("Money Withdrow Succesful");

            }


        }
    }
