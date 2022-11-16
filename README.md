# typing_speed
package speed_typing_calculator;
import java.util.Random;
import java.util.Scanner;
import java.util.concurrent.TimeUnit;
import java.time.LocalTime;

public class SpeedTypingCalculator {
	static String[] words= {"hello","ant","sandal","monkey","biscuit","rent","car","fun","rabbit","goat","ice"};

	public static void main(String[] args) throws InterruptedException {
		// TODO Auto-generated method stub
		System.out.println("3");
		TimeUnit.SECONDS.sleep(1);
		System.out.println("2");
		TimeUnit.SECONDS.sleep(1);
		System.out.println("1");
		TimeUnit.SECONDS.sleep(1);
		Random rand = new Random();
		for(int i=0;i<10;i++) {
			System.out.print(words[rand.nextInt(9)]+" ");
		}
		System.out.println();
		
		double start = LocalTime.now().toNanoOfDay();
		
		Scanner scan = new Scanner(System.in);
		String typedWords = scan.nextLine();
		
		double end = LocalTime.now().toNanoOfDay();
		double elapsedTime = end-start;
		double seconds = elapsedTime/1000000000.0;
		int numChars = typedWords.length();
		//(x characters/5)/1 min=y WPM
		int wpm=(int)((((double) numChars /5) /seconds) *60);
		
		System.out.println("your wpm is"+wpm+"!");
		
		}

}
