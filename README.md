# Ucak-Bileti-Hesaplama
---
Bu bir [patika.dev](www.patika.dev) projesidir.
```
import java.util.Scanner;
public class ucakBilet {
    public static void main(String[] args) {
        int age,select;
        double range,cost;
        Scanner input = new Scanner(System.in);
        System.out.print("Yolculuk Mesafesini Giriniz(km): ");
        range = input.nextInt();
        System.out.print("Yaşınızı Giriniz: ");
        age = input.nextInt();
        System.out.print("1.Tek Yön\n2.Gidiş Dönüş\nYolculuk Tipini Seçiniz:");
        select = input.nextInt();
        cost=range*(0.1);

        if (range>0 && age>0 && select>0 && select<3) {
            switch (select) {
                case 1:
                    if (age <= 12) {
                        cost = (cost * 0.5);
                    } else if (age > 12 && age < 24) {
                        cost = (cost * 0.9);
                    } else if (age > 65) {
                        cost = (cost * 0.7);
                    }else{
                        cost = cost;
                    }break;
                case 2:
                    if (age <= 12) {
                        cost = (cost * 0.5) * 1.6;
                    } else if (age > 12 && age < 24) {
                        cost = (cost * 0.9) * 1.6;
                    } else if (age > 65) {
                        cost = (cost * 0.7) * 1.6;
                    } else {
                        cost = cost*1.6;
                    }break;
            }
        }else {
            System.out.println("Hatalı Bir Giriş Yaptınız");
        }
            System.out.println("Ödeyeceğiniz Ücret: " + cost);
    }
}
```
