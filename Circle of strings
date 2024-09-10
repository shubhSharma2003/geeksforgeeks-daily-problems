class Solution {
public:
    void DFS(int node, vector<bool>& visited, vector<vector<int>>& adj) {
        visited[node] = true;
        
        for (auto v : adj[node]) {
            if (!visited[v])
                DFS(v, visited, adj);
        }
    }

    int isCircle(vector<string>& arr) {
        vector<int> inDeg(26, 0);
        vector<int> outDeg(26, 0);
        vector<vector<int>> adj(26);

        //Step 1 Create adjacency list
       //Step 2: Calculate indegree and outdegree of nodes simultaneously.


        for (auto A : arr) {
            int u = A[0] - 'a';
            int v = A[A.size() - 1] - 'a';
            
            adj[u].push_back(v);
            inDeg[v]++;
            outDeg[u]++;
        }
        //For eucleian Circuit to exist, indegree and outdegree of a node should be same.
        for (int i = 0; i < 26; i++) {
            if (inDeg[i] != outDeg[i])
                return false;
        }
        
       // Graph Traversal
        vector<bool> visited(26, false);
        int node = arr[0][0] - 'a';
        DFS(node, visited, adj);
        // check all nodes are visited or not.
        for (int i = 0; i < 26; i++) {
            if (inDeg[i] && !visited[i])
                return false;
        }
        
        return true;
    }
};
