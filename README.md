# interviewbit
public class Solution {
    public int coverPoints(ArrayList<Integer> A, ArrayList<Integer> B)
    {
        int count =0, a=A.get(0),b=B.get(0);
        for(int i =1 ; i< A.size() ; i++)
        {
            if(Math.abs(a-A.get(i))<=Math.abs(b-B.get(i)))
            { 
               count = count+Math.abs(a-A.get(i)); 
               count=count+(Math.abs(b-B.get(i))-Math.abs(a-A.get(i)));
               a=A.get(i);
               b=B.get(i);
                
            }
            else
            {
             
              count = count+Math.abs(b-B.get(i));
              count=count+(Math.abs(a-A.get(i))-Math.abs(b-B.get(i)));
                a=A.get(i);
               b=B.get(i);
                
            }
        }
        return count;
    }
}
