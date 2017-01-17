package Level1;

import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class NumberGenerator {
  public static void main(String[] args) throws IOException {
    BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
    int num = Integer.parseInt(br.readLine());
    int interval = Integer.parseInt(br.readLine());
    NumberGenerator n = new NumberGenerator();
    int[] tempResult = n.solve(interval, num);
    String result = tempResult.toString();
    System.out.print(result);

  }

  public int[] solve(int interval, int num) {
    int[] result = new int[interval];
    int starNum = num;
    result[0] = num;
    for(int i=1; i<interval; ++i) {
      int temp = starNum += num;
      result[i] = temp;
    }
    return result;
  }
}

------------------------------------------------------------------------------------------

package Level1;

import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class ConcealPhoneNumber {
  public static void main(String[] args) throws IOException {
    BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
    String strInput = br.readLine();
    String[] input = strInput.split("");
    ConcealPhoneNumber c = new ConcealPhoneNumber();
    String result = c.solve(input);
    System.out.print(result);
  }
  public String solve(String[] input) {
    int size = input.length;

    StringBuilder sb = new StringBuilder();
    for(int i=0; i<size; ++i) {
      if(i < size-4) {
        sb.append(input[i] = "*");
      }else {
        sb.append(input[i]);
      }
    }
    String result = sb.toString();
    return result;
  }
}




