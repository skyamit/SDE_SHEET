/****************************************************************

    Following is the class structure of the Pair class:

        class Pair
        {
        	int weight;
	        int value;
	        Pair(int weight, int value)
	        {
		        this.weight = weight;
		        this.value = value;
	        }
	        
        }
        
*****************************************************************/
import java.util.*;

public class Solution {
    public static double maximumValue(Pair[] items, int n, int w) {

        Arrays.sort(items,(Pair a,Pair b)->((b.value*100)/b.weight)-((a.value*100)/a.weight));
        
        double result = 0d;
        int i = 0;
        while(w>0 && i<items.length){
            int weight = items[i].weight;
            double value = (double)items[i].value;
            if(weight<=w){
                result += value;
                w -= weight;
            }
            else{
                result += (double)(value*((double)w/weight));
                w -= weight;
            }
            i++;
        }
        
        return result;
    }
}







