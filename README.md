<h1>Binary Trees</h1>
<img src= "https://user-images.githubusercontent.com/79994012/207780469-fe7d06d1-8e64-42c5-96e3-f2c52de029ac.jpg">

<p><strong>A Binary Tree</strong> is a hierarchical data structure in which each node has at most two children 
generally referred as left child and right child.</p>

<p>Each node contains three components:</p>
<ul>
<li>Pointer to left subtree</li>
<li>Pointer to right subtree</li>
<li>Data element</li>
</ul>
<p>The topmost node in the tree is called the root. An empty tree is represented by NULL pointer.</p>

<h2>Binary Tree: Common Terminologies</h2>
<ul>
 <li><strong>Root:</strong> Topmost node in a tree.</li>
 <li><strong>Parent:</strong> Every node (excluding a root) in a tree is connected by a directed edge from exactly one other node. 
This node is called a parent.</li>
 <li><strong>Child:</strong> A node directly connected to another node when moving away from the root.</li>
<li><strong>Leaf/External node:</strong> Node with no children.</li>
 <li><strong>Internal node:</strong> Node with atleast one children.</li>
<li><strong>Depth of a node:</strong> Number of edges from root to the node.</li>
 <li><strong>Height of a node:</strong> Number of edges from the node to the deepest leaf. Height of the tree is the height of the root.</li>
</ul><br>
<img src= "https://user-images.githubusercontent.com/79994012/207781951-3de5ee31-935c-411f-9834-1597858507a4.jpg">

<p>In the above binary tree we see that root node is <strong>A</strong>. The tree has 10 nodes with 5 internal nodes,
 i.e, <strong>A,B,C,E,G</strong> and 5 external nodes,
 i.e, <strong>D,F,H,I,J</strong>. The height of the tree is 3. 
 <strong>B</strong> is the parent of <strong>D</strong> and <strong>E</strong> while <strong>D</strong> and <strong>E</strong>
 are children of <strong>B</strong>.</p>
 
 <h2>Advantages of Trees</h2>
<p>Trees are so useful and frequently used, because they have some very serious advantages:<p>
<ul>
<li>Trees reflect structural relationships in the data.</li>
<li>Trees are used to represent hierarchies.</li>
<li>Trees provide an efficient insertion and searching.</li>
<li>Trees are very flexible data, allowing to move subtrees around with minumum effort.</li>
</ul>
<h2>Types of Binary Trees (Based on Structure)</h2>
<ul>
<li><strong>Rooted binary tree:</strong> It has a root node and every node has atmost two children.</li>
<li><strong>Full binary tree:</strong> It is a tree in which every node in the tree has either 0 or 2 children.</li>
<li><strong>Perfect binary tree:</strong> It is a binary tree in which all interior nodes have two children and all leaves have the same depth or same level.</li>
<li><strong>Complete binary tree:</strong> It is a binary tree in which every level, except possibly the last, is completely filled, and all nodes are as far left as possible.</li>

<li><strong>Balanced binary tree:</strong> A binary tree is height balanced if it satisfies the following constraints:</li>
<ul>
<li>The left and right subtrees' heights differ by at most one, AND</li>
<li>The left subtree is balanced, AND</li>
<li>The right subtree is balanced</li>
<li>An empty tree is height balanced.</li>
<li>The height of a balanced binary tree is O(Log n) where n is number of nodes.</li>
</ul>
<li><strong>Degenarate tree:</strong> It is a tree is where each parent node has only one child node. It behaves like a linked list.</li>
</ul>

<h2>Binary Search Tree</h2>
<p>A binary search tree is a useful data structure for fast addition and removal of data.

It is composed of nodes, which stores data and also links to upto two other child nodes. It is the relationship between the leaves linked to and the linking leaf, also known as the parent node, which makes the binary tree such an efficient data structure.

For a binary tree to be a binary search tree, the data of all the nodes in the left sub-tree of the root 
node should be less than the data of the root. The data of all the nodes in the right subtree of the root 
node should be greater than equal to the data of the root. As a result, the leaves on the farthest left
of the tree have the lowest values, whereas the leaves on the right of the tree have the greatest values.</p>

<h2>Insertion in a BST</h2>
<p>To insert data into a binary tree involves a function searching for an unused node in 
the proper position in the tree in which to insert the key value. The insert function is 
generally a recursive function that continues moving down the levels of a binary tree 
until there is an unused leaf in a position which follows the following rules of placing nodes.</p>
<ul>
<li>Compare data of the root node and element to be inserted.</li>
<li>If the data of the root node is greater, and if a left subtree exists, 
then repeat step 1 with root = root of left subtree. Else,</li>
<li>Insert element as left child of current root.</li>
<li>If the data of the root node is greater, and if a right subtree exists, 
then repeat step 1 with root = root of right subtree.</li>
<li>Else, insert element as right child of current root. </li>
</ul>
 
 <h2>Searching in a BST</h2>
<p>The search function works in a similar fashion as insert. 
It will check if the key value of the current node is the value to be searched.
 If not, it should check to see if the value to be searched for is less than the value of the node, 
 in which case it should be recursively called on the left child node, 
 or if it is greater than the value of the node, it should be recursively called on the right child node.</p>
<ul>
<li>Compare data of the root node and the value to be searched.</li>
<li>If the data of the root node is greater, and if a left subtree exists, 
then repeat step 1 with root = root of left subtree. Else,</li>
<li>If the data of the root node is greater, and if a right subtree exists,
then repeat step 1 with root = root of right subtree. Else,</li>
<i>If the value to be searched is equal to the data of root node, return true.</li>
<li>Else, return false.</li>
</ul>

<h2>Traversing in a BST</h2>
<p>There are mainly three types of tree traversals:</p>
<h3>Pre-order Traversal:</h3>
<p>In this technique, we do the following :</p>
<ul>
<li>Process data of root node.</li>
<li>First, traverse left subtree completely.</li>
<li>Then, traverse right subtree.</li>
</ul>


<h3>Post-order Traversal:</h3>
<p>In this traversal technique we do the following:</p>
<ul>
<li>First, traverse left subtree completely.</li>
<li>Then, traverse right subtree completely.</li>
<li>Then, process data of node.</li>
</ul>


<h3>In-order Traversal:</h3>
<p>In in-order traversal, we do the following:</p>
<ul>
<li>First process left subtree.</li>
<li>Then, process current root node.</li>
<li>Then, process right subtree.</li>
</ul>
 
 <a href= "https://www.studytonight.com/data-structures/introduction-to-binary-trees" target="_blank">READ More(From Src)</a>

