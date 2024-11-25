import java.util.Scanner;

public class QuizApplication {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Quiz questions and answers
        String[] questions = {
            "1. What is the capital of India?\n   a) Mumbai\n   b) Delhi\n   c) Bangalore\n   d) Chennai",
            "2. Who invented Java Programming?\n   a) Dennis Ritchie\n   b) James Gosling\n   c) Guido van Rossum\n   d) Bjarne Stroustrup",
            "3. What is the correct extension of Java files?\n   a) .java\n   b) .py\n   c) .class\n   d) .txt"
        };
        char[] answers = {'b', 'b', 'a'};

        int score = 0;

        // Loop through the questions
        for (int i = 0; i < questions.length; i++) {
            System.out.println(questions[i]);
            System.out.print("Your answer: ");
            char userAnswer = scanner.next().charAt(0);

            // Check if the answer is correct
            if (userAnswer == answers[i]) {
                System.out.println("Correct!\n");
                score++;
            } else {
                System.out.println("Wrong! The correct answer is: " + answers[i] + "\n");
            }
        }

        // Display the final score
        System.out.println("Quiz Finished!");
        System.out.println("Your final score is: " + score + "/" + questions.length);

        // Feedback based on score
        if (score == questions.length) {
            System.out.println("Excellent! You got all answers right!");
        } else if (score > 0) {
            System.out.println("Good job! Keep practicing to improve.");
        } else {
            System.out.println("Better luck next time!");
        }

        scanner.close();
    }
}
