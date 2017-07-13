# Oprec
package com.company;

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        String tampung = "";
        String jawab = "";

        do {
            System.out.println("==== Program Palindrom ====");
            System.out.print("Masukkan kata : ");
            String kata = scan.next();

            for (int i = 0; i < kata.length() / 2; i++) {
                if (kata.charAt(i) != kata.charAt(kata.length() - i - 1)) {
                    tampung = "false";
                } else {
                    tampung = "true";
                }
            }
            if (tampung.equals("false")) {
                System.out.println(kata + " = false");
            } else {
                System.out.println(kata + " = true");
            }
            System.out.print("Apakah ingin mencoba lagi ? (y/t) ");
            jawab=scan.next();

        }while (jawab.equals("y"));
        System.out.println("======Terima Kasih======");
    }
}
