import java.time.LocalDate;
import java.time.Period;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);


        System.out.println("Masukkan Nama:");
        String nama = scanner.nextLine();

        System.out.println("Masukkan Jenis Kelamin (P/L):");
        String jenisKelamin = scanner.nextLine();
        jenisKelamin = jenisKelamin.equalsIgnoreCase("P") ? "Perempuan" : "Laki-laki";

        System.out.println("Masukkan Tanggal Lahir (YYYY-MM-DD):");
        String tanggalLahirStr = scanner.nextLine();
        LocalDate tanggalLahir = LocalDate.parse(tanggalLahirStr);


        LocalDate today = LocalDate.now();
        Period period = Period.between(tanggalLahir, today);
        int umur = period.getYears();


        System.out.println("\nData Diri:");
        System.out.println("Nama: " + nama);
        System.out.println("Jenis Kelamin: " + jenisKelamin);
        System.out.println("Tanggal Lahir: " + tanggalLahir);
        System.out.println("Umur: " + umur + " tahun");

        scanner.close();
    }
}
