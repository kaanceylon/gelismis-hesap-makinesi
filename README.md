# gelismis-hesap-makinesi
import java.awt.*;
import java.sql.PreparedStatement;
import java.util.Scanner;

public class Main {
    static int sum (int a, int b){
        int result = a+b;
        System.out.print("Toplam: "+ result);
        return result;
    }
    static int minus(int a, int b){
        int result = a-b;
        System.out.print("Çıkarma: "+ result);
        return result;
    }
    static int times(int a, int b){
        int result = a*b;
        System.out.print("Çarpma: " + result);
        return result;
    }
    static int divide(int a, int b){
        int result = a/b;
        System.out.print("Bölme: "+ result);
        return result;
    }
    static int power(int a, int b){
        int result =1;
        for (int i=1; i<=b; i++){
            result*=a;
        }
        System.out.print("Üs işlemi: "+ result);
        return result;
    }
    static int mod(int a, int b){
        int result = a % b;
        System.out.print("mod: "+ result);
        return result;
    }
    static void calc(int a, int b){
        System.out.print("Çevresi: " + (2*(a+b)));
        System.out.print("Alanı: " + (a*b));
    }



    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        int select;

        String menu = "1.Toplama\n" + "2.Cikarma\n" + "3.Carpma\n" + "4.Bolme\n"
                + "5.Uslu Sayi\n" + "6.Mod Alma\n" + "7.Dikdortgen Alan Cevre\n"
                + "0.Cikis";
        while (true){
            System.out.println(menu);
            System.out.println("Bir işlem seçiniz : ");
            select = input.nextInt();

            if (select== 0){
                break;
            }
            System.out.print("İlk sayiyi giriniz: ");
            int a = input.nextInt();
            System.out.print("İkinci sayiyi giriniz: ");
            int b = input.nextInt();

            switch (select){

                case 1:
                    sum(a,b);
                    break;
                case 2:
                    minus(a,b);
                    break;
                case 3:
                    times(a,b);
                    break;
                case 4:
                    divide(a,b);
                    break;
                case 5:
                    power(a,b);
                    break;
                case 6:
                    mod(a,b);
                    break;
                case 7:
                    calc(a,b);
                    break;
                default:
                    System.out.print("Geçersiz bir işlem yaptınız!!!");



            }

        }


    }
}
































