Write a function that sums up the digits of a number. Try to implement it both iteratively and recursively.

<pre>
  <code class="prettyprint">
def sum_digits(n):
    """
    Takes a number n as input and outputs the 
    sum of the digits of n.
    
    >>> sum_digits(100)
    1
    >>> sum_digits(235)
    10
    """
    "***YOUR CODE HERE***"
  </code>
</pre>

{% if page.solution %}
<button onclick="toggleSolution()">Toggle Solution</button>

<div class="solution">
  <pre>
    <code class="prettyprint">
def sum_digits(n):
    """
    Takes a number n as input and outputs the 
    sum of the digits of n.
    
    >>> sum_digits(100)
    1
    >>> sum_digits(235)
    10
    """
    if n < 10:
        return n
    return n % 10 + sum_digits(n // 10)
    </code>
  </pre>
  
  <p>
    When we are given a number, n, that is less than 10, we know that the number has only one digit so we can just return that number. When it is greater than or equal to ten, we want to mod it by 10 to get the ones place, and then remove the ones place and use recursion to find the sum of the rest of the digits. The floordiv operator allows us to remove the ones place from the number by floordiving by 10.
  </p>
</div>
{% endif %}