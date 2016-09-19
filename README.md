# maxRun
This program calculates the the length of the largest run in the string and displays it.

/****************************************************************************
 *
 * Created by: Ryan St. Louis
 * Created on: September 18th, 2016
 * This program calculates the the length of the largest run in the string,
 * and displays it.
 *
 ****************************************************************************/

class Main {
  public static void main(String[] args) {
String target = "xxyyyyyzz";
int maxCount = 0;
int runCount = 1;
char previous = '\u0000';  //default empty char
for (int pos=0; pos<target.length(); pos++) {
    if ( target.charAt(pos) == previous ) {
        runCount++;
        if (runCount > maxCount) {  //if we have exceeded our max run now
            maxCount = runCount;
        }
    } else {
        runCount = 1;  //reset to a new run.
    }
    previous = target.charAt(pos);  //reassign the previous before next iteration
}
System.out.println(maxCount);
  }
}
