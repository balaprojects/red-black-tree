# Red Black Tree

>What is Red Black Tree
   - It is a self balancing binary search tree.
   - Compared to AVL tree, in this tree we do less number of rotation which is why is preferred in most cases.
   - TreeMap or SortedMap in java uses this algorithm.

>Rules to determine whether a given tree is valid Red Black Tree
   - Root is black
   - No **red-red** parent child
   - Number of black nodes in every path of the tree from root to leaf is same.

>Rules for insertion into Red Black Tree
   - If empty create a black root node.
   - Insert new leaf node as red
      - If its parent is black we are done
      - If its parent is red
          - If the node's sibling is absent or black then rotate, recolor and done.
              - Get the node and it parent position.
                  - LL - Right rotation on node's parent. ***New root becomes black and old root becomes red.***
                  - LR - Right rotation on node and left rotation on parent.
                  - RL - Left rotation on node and right rotation on parent.
                  - RR - Left rotation on node's parent.
          - If the node's sibling is red then just recolor. Recolor the node and its sibling to black and if the parent is black and not root then color it red.
 
>See the picture and write code
  
   ![](https://github.com/balaprojects/images/blob/master/Red-Black-1.png)

>How to do deletion in Red-Black tree
   - Convert to 0 or 1 child case.
   - If the node to be deleted is red or child is red then replace.
   - Double black node has 6 cases.
   - ![](https://github.com/balaprojects/images/blob/master/DoubleBlack_Cases.png)
