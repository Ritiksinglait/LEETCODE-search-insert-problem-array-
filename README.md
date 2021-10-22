# LEETCODE-search-insert-problem-array-
 QUESTION : - Given a sorted array of distinct integers and a target value, return the index if the target is found. If not, return the index where it would be if it were inserted in order.
 Example 1:

Input: nums = [1,3,5,6], target = 5
Output: 2
Example 2:

Input: nums = [1,3,5,6], target = 2
Output: 1
Example 3:

Input: nums = [1,3,5,6], target = 7
Output: 4
 
answer  : -
 
 
 
 
 
 
 class Solution{
    static int searchInsert(int[] nums, int target) {
      if(target>nums[nums.length-1]){
        return nums.length;
    }
 
    int l=0;
    int r=nums.length-1;
 
    while(l<r){
        int m = l+(r-l)/2;
        if(target>nums[m]){
            l=m+1;
        }else{
            r=m;
        }
    }
 
    return l;
    }    
        
        public static void main(String[] args)
    {
        int nums[] = { 1, 3,5,6};
        int val=2;
  
      int  x = searchInsert(nums,val);
  
        // Printing The array elements
         
        for (int i = 0; i < x; i++)
            System.out.print(nums[i] + " ");
    
    }
}
 

