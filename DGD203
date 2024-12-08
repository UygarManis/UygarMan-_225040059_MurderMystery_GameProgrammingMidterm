using System;

class MurderMystery
{
    static void Main(string[] args)
    {
        Console.WriteLine("Hello, detective! A mysterious murder case awaits you. May I know your name first?\n");
        string name = Console.ReadLine();

        Console.WriteLine($"Welcome, {name}. A wealthy family has requested your help to solve a murder in their mansion. Let's get started!\n");
        int score = 0;

        // 1. Soru
        Console.WriteLine($"» {name}, you arrive at the mansion and are greeted by the butler. Where would you like to start your investigation?\n");
        Console.WriteLine("A-) Search the victim's study\nB-) Interview the staff in the kitchen\n");
        char choice1 = GetUserChoice();

        if (choice1 == 'A')
        {
            Console.WriteLine($"{name}, in the study, you find a strange letter with a cryptic message.\n");
            score += 5;

            // 2. Soru
            Console.WriteLine($"» {name}, the letter leads you to two possible clues:\n");
            Console.WriteLine("A-) Go to the garden and search for more clues\nB-) Search the library for hidden information\n");
            char choice2A = GetUserChoice();

            if (choice2A == 'A')
            {
                Console.WriteLine($"{name}, in the garden, you find a torn piece of fabric and a mysterious footprint.\n");
                score += 4;
            }
            else if (choice2A == 'B')
            {
                Console.WriteLine($"{name}, in the library, you find a hidden journal that could provide vital information.\n");
                score += 6;
            }
        }
        else if (choice1 == 'B')
        {
            Console.WriteLine($"{name}, the kitchen staff is nervous, but one of them mentions a strange figure seen near the victim's room.\n");
            score += 3;

            Console.WriteLine($"» {name}, you gather information from the staff. Two suspects stand out:\n");
            Console.WriteLine("A-) Investigate the victim's close friend who was often in the mansion\nB-) Investigate the mysterious figure seen near the room\n");
            char choice2B = GetUserChoice();

            if (choice2B == 'A')
            {
                Console.WriteLine($"{name}, the friend is an unreliable source, but they mention a hidden room in the mansion.\n");
                score += 4;
            }
            else if (choice2B == 'B')
            {
                Console.WriteLine($"{name}, the mysterious figure leads you to a hidden hallway and a locked door.\n");
                score += 6;
            }
        }

        // 3. Soru
        Console.WriteLine($"» {name}, after gathering your clues, you suspect one of the family members. It's time to confront the person behind the murder.\n");
        Console.WriteLine("A-) Confront them with the evidence\nB-) Continue to search for more evidence to be sure\n");
        char choice3 = GetUserChoice();

        if (choice3 == 'A')
        {
            Console.WriteLine($"{name}, you confronted the suspect. They broke down and confessed, but it was a trap!\n");
            score += 4;
            Console.WriteLine($"{name}, you were caught in the trap and... you died.\n");
            score = 0;  
            Console.WriteLine("Unfortunately, you've lost. Let's start over.\n");
            Main(args); 
            return; 
        }
        else if (choice3 == 'B')
        {
            Console.WriteLine($"{name}, you uncovered a hidden secret that helped you solve the case with more certainty.\n");
            score += 6;
        }

        // Final
        Console.WriteLine($"» {name}, finally, you discover the true identity of the murderer, and you are led to a secret room where the final confrontation occurs.\n");
        Console.WriteLine("A-) Risk everything to confront the murderer\nB-) Use your wits to capture them without danger\n");
        char choice4 = GetUserChoice();

        if (choice4 == 'A')
        {
            Console.WriteLine($"{name}, you captured the murderer, but you were nearly trapped in the secret room.\n");
            score += 0;
        }
        else if (choice4 == 'B')
        {
            Console.WriteLine($"{name}, you successfully captured the murderer without a struggle, avoiding danger.\n");
            score += 7;
        }

        // Final Results
        Console.WriteLine($"Congratulations, {name}. You completed the case! Let's see how you performed:");
        if (score >= 25)
        {
            Console.WriteLine("You are an outstanding detective! Not only did you solve the case, but you also caught the murderer without danger.");
        }
        else if (score >= 15)
        {
            Console.WriteLine("You did a good job. You solved the case, but there was room for improvement.");
        }
        else
        {
            Console.WriteLine("Unfortunately, you failed. But don't worry, you can try again and do better next time.");
        }
    }

    static char GetUserChoice()
    {
        char choice;

        do
        {
            Console.WriteLine("Please choose A or B:");
            choice = Console.ReadKey().KeyChar;
            Console.WriteLine(); 
        } while (choice != 'A' && choice != 'a' && choice != 'B' && choice != 'b');

        return char.ToUpper(choice); 
    }
}
