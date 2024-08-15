class Solution {
    public boolean isSubsequence(String s, String t) {
        int n= s.length();
        int m= t.length();
        int i= 0;
        for(int j=0; j< m; j++){
            if(i == n) return true; // uf i reaches n means all chars of s are present in t
            if(t.charAt(j) == s.charAt(i)){ // if char matched then increase i by 1
                i++;
            }
        }
        return i == n;
    }
}
