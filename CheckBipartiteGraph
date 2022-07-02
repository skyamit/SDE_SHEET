import java.util.*;

public class Solution {

    public static boolean isGraphBirpatite(ArrayList<ArrayList<Integer>> edges) {
        ArrayList<ArrayList<Integer>> adjList =new ArrayList<>();
        int size =edges.size();
        for(int i=0;i<size;i++){
            adjList.add(new ArrayList<>());
        }
        
        for(int i=0;i<size;i++){
            for(int j=0;j<size;j++){
                if(edges.get(i).get(j)==1){
                    adjList.get(i).add(j);
                    adjList.get(j).add(i);
                }
            }
        }
        
        int[] color = new int[size];
        for(int i=0;i<size;i++){
            if(color[i]==0){
                if(!bfs(i,color,adjList))
                    return false;
            }
        }
        return true;
    }
    public static boolean bfs(int curr, int[] color,ArrayList<ArrayList<Integer>> adjList){
        Queue<Integer> queue = new LinkedList<>();
        color[curr] = 1;
        queue.offer(curr);
        
        while(!queue.isEmpty()){
            int top = queue.poll();
            for(Integer x : adjList.get(top)){
                if(color[x]==0){
                    color[x] = 3 - color[top];
                    queue.offer(x);
                }
                else if(color[x]==color[top])
                    return false;
            }
        }
        return true;
    }
}
