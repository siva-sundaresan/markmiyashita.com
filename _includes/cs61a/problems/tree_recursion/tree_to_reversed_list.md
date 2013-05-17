<p>
  This problem uses the <a href="http://markmiyashita.com/cs61a/code/tree_recursion/tree.py">Tree class</a> and the template for this file can be downloaded <a href="http://markmiyashita.com/cs61a/code/tree_recursion/tree_to_reversed_list.py">here.</a>
</p>

<p>
  In this problem, the input is a binary tree and the output is a list. The list is formed by getting the rightmost entry first. If you haven't already, the traversal questions located <a href="http://markmiyashita.com/cs61a/sp13/problems/trees_trees_everywhere/">here</a> may help you.
</p>

<pre>
  <code class="prettyprint">
def tree_to_reversed_list(tree):
    """
    >>> t = Tree(5, Tree(1, None, Tree(4)), Tree(7, Tree(6), Tree(8)))
    >>> tree_to_reversed_list(t)
    [8, 7, 6, 5, 4, 1]
    """
    "***YOUR CODE HERE***"
  </code>
</pre>

{% if page.solution %}
<button onclick="toggleSolution()">Toggle Solution</button>

<div class="solution">
  <pre>
    <code class="prettyprint">
def tree_to_reversed_list(tree):
    """
    >>> t = Tree(5, Tree(1, None, Tree(4)), Tree(7, Tree(6), Tree(8)))
    >>> tree_to_reversed_list(t)
    [8, 7, 6, 5, 4, 1]
    """
    lst = []
    if tree is not None:
        if tree.right:
            lst.extend(tree_to_reversed_list(tree.right))
        lst.append(tree.entry)
        if tree.left:
            lst.extend(tree_to_reversed_list(tree.left))
    return lst
    </code>
  </pre>
  
  <p>
    
  </p>
</div>
{% endif %}