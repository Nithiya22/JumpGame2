# JumpGame2
class Solution {
    public int jump(int[] nums) {
        if(nums.length==1){
            return 0;
        }
         int finalposition=nums.length-1;
         int coverage=0;
         int lastindex=0;
         int jump=0;
         for(int i=0;i<nums.length;i++){
             coverage=Math.max(coverage,i+nums[i]);
         
         if(i==lastindex){
             lastindex=coverage;
             jump++;
             if(lastindex==finalposition){
                 return jump;
             }
         }
         }
        return jump;
    }
}
