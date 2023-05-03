Download Link: https://assignmentchef.com/product/solved-cs210-project-2
<br>
<table width="720">

 <tbody>

  <tr>

   <td width="165">LinkedDeque()</td>

   <td width="555">construct an empty deque</td>

  </tr>

  <tr>

   <td width="165">boolean isEmpty()</td>

   <td width="555">is the deque empty?</td>

  </tr>

  <tr>

   <td width="165">int size()</td>

   <td width="555">the number of items on the deque</td>

  </tr>

  <tr>

   <td width="165">void addFirst(Item item)</td>

   <td width="555">add <em>item </em>to the front of the deque</td>

  </tr>

  <tr>

   <td width="165">void addLast(Item item)</td>

   <td width="555">add <em>item </em>to the end of the deque</td>

  </tr>

  <tr>

   <td width="165">Item removeFirst()</td>

   <td width="555">remove and return the item from the front of the deque</td>

  </tr>

  <tr>

   <td width="165">Item removeLast()</td>

   <td width="555">remove and return the item from the end of the deque</td>

  </tr>

  <tr>

   <td width="165">Iterator&lt;Item&gt; iterator()</td>

   <td width="555">an iterator over items in the deque in order from front to end</td>

  </tr>

  <tr>

   <td width="165">String toString()</td>

   <td width="555">a string representation of the deque</td>

  </tr>

 </tbody>

</table>

<em>Corner cases. </em>Throw a java.lang.NullPointerException if the client attempts to add a null item;

throw a java.util.NoSuchElementException if the client attempts to remove an item from an empty deque; throw a

java.lang.UnsupportedOperationException if the client calls the remove() method in the iterator; throw a

java.util.NoSuchElementException if the client calls the next() method in the iterator and there are no more items to return.

<em>Performance requirements. </em>Your deque implementation must support each deque operation (including construction) in constant worst-case time and use space proportional to linear in the number of items currently in the deque. Additionally, your iterator implementation must support each operation (including construction) in constant worst-case time.

<table width="720">

 <tbody>

  <tr>

   <td width="720">$ java LinkedDeque false(364 characters) There is grandeur in this view of life, with its several powers, having been originally breathed into a few forms or into one; and that, whilst this planet has gone cycling on according to the fixed law of gravity, from so simple a beginning endless forms most beautiful and most wonderful have been, and are being, evolved. ~ Charles Darwin, The Origin of Species true</td>

  </tr>

 </tbody>

</table>

<strong>Problem 2. </strong>(<em>Random Queue</em>) A random queue is similar to a stack or queue, except that the item removed is chosen uniformly at random from items in the data structure. Create a generic iterable data type ResizingArrayRandomQueue&lt;Item&gt; in ResizingArrayRandomQueue.java that uses a resizing array to implement the following random queue API:

<h1>method                                          description</h1>

<table width="720">

 <tbody>

  <tr>

   <td width="171">ResizingArrayRandomQueue()</td>

   <td width="549">construct an empty queue</td>

  </tr>

  <tr>

   <td width="171">boolean isEmpty()</td>

   <td width="549">is the queue empty?</td>

  </tr>

  <tr>

   <td width="171">int size()</td>

   <td width="549">the number of items on the queue</td>

  </tr>

  <tr>

   <td width="171">void enqueue(Item item)</td>

   <td width="549">add <em>item </em>to the queue</td>

  </tr>

  <tr>

   <td width="171">Item dequeue()</td>

   <td width="549">remove and return a random item from the queue</td>

  </tr>

  <tr>

   <td width="171">Item sample()</td>

   <td width="549">return a random item from the queue, but do not remove it</td>

  </tr>

  <tr>

   <td width="171">Iterator&lt;Item&gt; iterator()</td>

   <td width="549">an independent iterator over items in the queue in random order</td>

  </tr>

  <tr>

   <td width="171">String toString()</td>

   <td width="549">a string representation of the queue</td>

  </tr>

 </tbody>

</table>

<strong>1 of 2</strong>

<h1></h1>

The order of two or more iterators to the same randomized queue must be mutually independent; each iterator must maintain its own random order.

<em>Corner cases. </em>Throw a java.lang.NullPointerException if the client attempts to add a null item;

throw a java.util.NoSuchElementException if the client attempts to sample or dequeue an item from an empty randomized queue; throw a java.lang.UnsupportedOperationException if the client calls the remove() method in the iterator; throw a java.util.NoSuchElementException if the client calls the next() method in the iterator and there are no more items to return.

<em>Performance requirements. </em>Your randomized queue implementation must support each randomized queue operation (besides creating an iterator) in constant amortized time and use space proportional to linear in the number of items currently in the queue. That is, any sequence of <em>M </em>randomized queue operations (starting from an empty queue) must take at most <em>cM </em>steps in the worst case, for some constant <em>c</em>. Additionally, your iterator implementation must support next() and hasNext() in constant worst-case time and construction in linear time; you may use a linear amount of extra memory per iterator.

<table width="720">

 <tbody>

  <tr>

   <td width="720">$ java ResizingArrayRandomQueue1 2 3 4 5 6 7 8 9 10&lt;ctrl-d&gt;55 0 55 true</td>

  </tr>

 </tbody>

</table>

<strong>Problem 3. </strong>(<em>Subset</em>) Write a client program Subset.java that takes a command-line integer <em>k</em>, reads in a sequence of strings from standard input using StdIn.readString(), and prints out exactly <em>k </em>of them, uniformly at random. Each item from the sequence can be printed out at most once. You may assume that 0 ≤ <em>k </em>≤ <em>N</em>, where <em>N </em>is the number of strings on standard input. The running time of the program must be linear in the size of the input. You may use only a constant amount of memory plus either one LinkedDeque or ResizingArrayRandomQueue object of maximum size at most <em>N</em>.

$ java Subset 3

A B C D E F G H I

&lt;ctrl-d&gt;

G

I

E

$ java Subset 3

A B C D E F G H I

&lt;ctrl-d&gt;

F

D

E

$ java Subset 8 AA BB BB BB BB BB CC CC

&lt;ctrl-d&gt;

BB

CC

AA

BB

BB

BB

CC

BB

<strong>Acknowledgements </strong>This project is an adaptation of the Deques and Randomized Queues assignment developed at Princeton University by Kevin Wayne.