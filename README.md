# second-largest-code

import java.util.*;
public class Main
{
    public static int SecondLargest(int[] arr){
        int first_max=-1, second_max=-1;
        int n = arr.length;
        for(int i=0;i<n;i++){
            if(arr[i]>first_max){
                first_max =arr[i];
            }
        }
        for(int i=0;i<n;i++){
            if(arr[i]>second_max && arr[i]!=first_max){
                second_max =arr[i];
            }
        }
        return second_max; // returns -1 if no second largest found
    }
	public static void main(String[] args) {
	    //Input: [3, 5, 2, 5, 6, 6, 1]
        //Output: 5
        
        //Input: [7, 7, 7]
        //Output: -1
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter size:");
        int size= sc.nextInt();
        int[] arr = new int[size];
        for(int i=0;i<size;i++){
            arr[i] = sc.nextInt();
        }
        
		System.out.println("Second Largest:" +SecondLargest(arr));
	}
}
