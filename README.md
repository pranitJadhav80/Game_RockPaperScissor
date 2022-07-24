# Game_RockPaperScissor
package com.company;
import java.util.Scanner;
import java.util.Random;

public class cwh_20_Game {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter user's input : ");
        int user_inp = sc.nextInt(3);

        Random sd = new Random();
        System.out.println("Enter computer's input : ");
        int comp_inp = sd.nextInt(3);

        String user_move, comp_move;

        if (comp_inp == 0) {
            comp_move = "Rock";
        }
        else if (comp_inp == 1) {
            comp_move = "Paper";
        }
        else {
            comp_move = "Scissor";
        }

        switch(user_inp){
            case 0:
                System.out.println("YOU      : " + "  +  " + "ROCK");
                System.out.println("           vs          ");
                System.out.println("COMPUTER : " + comp_move);
                break;

            case 1:
                System.out.println("YOU      : " + "  +  " + "PAPER");
                System.out.println("           VS          ");
                System.out.println("COMPUTER : " + comp_move);
                break;

            case 2:
                System.out.println("YOU      : " + "  +  " + "SCISSOR");
                System.out.println("           VS          ");
                System.out.println("COMPUTER : " + comp_move);
                break;
        }

        if(comp_inp == user_inp){
            System.out.println("\nMATCH DRAW..........!");
        }

        else if((user_inp == 0 && comp_inp == 2) || (user_inp == 1 && comp_inp == 0) || (user_inp == 2 && comp_inp== 1)){
            System.out.println("\nYOU WON.............!");
        }

        else{
            System.out.println("\nCOMPUTER WON........!");
        }


    }
}
