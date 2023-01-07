import java.util.Scanner;


public class UcakBileti {

    public static void main(String[] args){

        Scanner input = new Scanner(System.in);
        int km,yas,yolcuTipi;
        double mesafeUcret = 0.10;
        double normal;
        double odenecekTutar;

        System.out.println("Kaç KM Gideceksiniz");
        km = input.nextInt();
        System.out.println("Yaş Bilginizi Giriniz");
        yas = input.nextInt();
        System.out.println("Yolculuk Tipini Giriniz ( 1 => Yek Yön, 2 => Gidiş Dönüş)");
        yolcuTipi = input.nextInt();

        normal = (km * mesafeUcret);

        switch (yolcuTipi) {

            case 1:
                if (yas >0 && yas < 12){
                    odenecekTutar = normal * 0.5;
                    System.out.println("Toplam Tutar = " + odenecekTutar);
                } else if (yas >=12 && yas <24) {
                    odenecekTutar = normal * 0.90;
                    System.out.println("Toplam Tutar = " + odenecekTutar);

                } else if (yas >= 25 && yas<64) {
                    odenecekTutar = normal;
                    System.out.println("Toplam Tutar = " + odenecekTutar);

                } else if (yas >= 65) {
                    odenecekTutar = normal * 0.70;
                    System.out.println("Toplam Tutar = " + odenecekTutar);

                } else {
                    System.out.println("Hatalı Veri Girişi");
                }
                break;
            case 2 :
                if (yas >0 && yas < 12){
                    odenecekTutar = (normal * 0.5)*0.80*2;
                    System.out.println("Toplam Tutar = " + odenecekTutar);

                } else if (yas >=12 && yas <24) {
                    odenecekTutar = (normal * 0.90)*0.80*2;
                    System.out.println("Toplam Tutar = " + odenecekTutar);

                } else if (yas >= 25 && yas<64) {
                    odenecekTutar = normal*0.80*2;
                    System.out.println("Toplam Tutar = " + odenecekTutar);

                } else if (yas >= 65) {
                    odenecekTutar = (normal * 0.70)*0.80*2;
                    System.out.println("Toplam Tutar = " + odenecekTutar);

                } else {
                    System.out.println("Hatalı Veri Girişi");

                }
                break;
            default:
                System.out.println("Hatalı Yolcu Tipi Seçimi");
                break;
        }







    }



}
