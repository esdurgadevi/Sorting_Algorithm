# Sorting_Algorithm
### Selection Sort
- Get the minimum Element to first 
```java
import java.util.Scanner;
public class Main
{
	public static void main(String[] args) {
	    Scanner sc=new Scanner(System.in);
	    int n=sc.nextInt();
	    int[] arr=new int[n];
	    for(int i=0;i<n;i++) arr[i]=sc.nextInt();
	    Selection_sort(arr,n);
	     for(int i=0;i<n;i++) System.out.print(arr[i]+" ");
	}
	public static void Selection_sort(int[] arr,int n){
	    for(int i=0;i<n-1;i++){
	        int min=i;
	        for(int j=i+1;j<n;j++){
	            if(arr[min]>arr[j]) min=j;
	        }
	        int t=arr[i];
	        arr[i]=arr[min];
	        arr[min]=t;
	    }
	}
}
```
- The steps involved this algorithm is n-2 here n is the number of elements so i put the outer for loop <n-1 so it will run 0 to 4
- Initially i set the minimum value as the index o then i compare all the values next to the index i and get the minimum value index after complete the inner loop i wap the minimmum value
  to the current indext position.
- In the sorting algorithm will run for n times that is
      1.first time run 0 to n-1
      2.Second time run 1 to n-1
      3.third time run 2 to n-1 and so on
- So the time Complexity is n+(n-1)+(n-2)+.... = n(n-1)/2 = n<sup>2</sup>/2 * n/2 neglect the small terms and constant we get n<sup>2</sup> 
- Time Compleity : o(n<sup>2</sup>)
### Bubble Sort
- Check the adjacent element
- Push the maximum element to last
```java
import java.util.Scanner;
public class Main
{
	public static void main(String[] args) {
	    Scanner sc=new Scanner(System.in);
	    int n=sc.nextInt();
	    int[] arr=new int[n];
	    for(int i=0;i<n;i++) arr[i]=sc.nextInt();
	    Bubble_sort(arr,n);
	     for(int i=0;i<n;i++) System.out.print(arr[i]+" ");
	}
	public static void Bubble_sort(int[] arr,int n){
	    for(int i=1;i<n;i++){
	        int swap=0;
	        for(int j=0;j<n-i;j++){
	            if(arr[j]>arr[j+1]){
	                int t=arr[j];
	                arr[j]=arr[j+1];
	                arr[j+1]=t;
	                swap=1;
	            }
	        }if(swap==0) break;
	    }
	}
}
```
- Time complexity :
    For Worst case : o(n<sup>2</sup>)
    For Best Case : o(n)
- For best case we use swap variable if the array is already in sorted order then it will break the loop this is the best case.
### Insertion Sort
- Take a element and place in a correctposition
```java
import java.util.Scanner;
public class Main
{
	public static void main(String[] args) {
	    Scanner sc=new Scanner(System.in);
	    int n=sc.nextInt();
	    int[] arr=new int[n];
	    for(int i=0;i<n;i++) arr[i]=sc.nextInt();
	    Insertion_sort(arr,n);
	     for(int i=0;i<n;i++) System.out.print(arr[i]+" ");
	}
	public static void Insertion_sort(int[] arr,int n){
	    for(int i=0;i<n;i++){
	        int j=i;
	        while(j>0 && arr[j-1]>arr[j])
	        {
	            int t=arr[j-1];
	            arr[j-1]=arr[j];
	            arr[j]=t;
	            j--;
	        }
	    }
	}
}
```
- Time complexity :
    For Worst case : o(n<sup>2</sup>)
    For Best Case : o(n)
[Slection,Bubble,Insertion](https://www.youtube.com/watch?v=HGk_ypEuS24&list=PLgUwDviBIf0oF6QL8m22w1hIDC1vJ_BHz&index=14)
### Merge Sort
[Merge Sort](https://www.youtube.com/watch?v=ogjf7ORKfd8&list=PLgUwDviBIf0oF6QL8m22w1hIDC1vJ_BHz&index=15)


  
  
