Download Link: https://assignmentchef.com/product/solved-cse222-homework-5
<br>
<strong><u>PART 1 </u></strong>

Write a custom iterator class MapIterator to iterate through the keys in a HashMap data structure in Java. This class should have the following methods:

<ul>

 <li>next(): The function returns the next key in the Map. It returns the first key when there is no not-iterated key in the Map.</li>

</ul>




<ul>

 <li>prev(): The iterator points to the previous key in the Map. It returns the last key when the iterator is at the first key.</li>

</ul>




<ul>

 <li>hasNext(): The method returns True if there are still not-iterated key/s in the Map, otherwise returns False.</li>

</ul>




<ul>

 <li>MapIterator (K key): The iterator should start from the given key and still iterate though all the keys in the Map. The iterator starts from any key in the Map when the starting key is not in the Map or not specified (zero parameter constructor).</li>

</ul>

<strong> </strong>

<strong><u>PART 2 </u></strong>

Implement KWHashMap interface in the book using the following hashing methods to organize hash table:

<ul>

 <li>Use the chaining technique for hashing by using linked lists (available in the text book) to chain items on the same table slot.</li>

</ul>




<ul>

 <li>Use the chaining technique for hashing by using TreeSet (instead of linked list) to chain items on the same table slot.</li>

</ul>




<ul>

 <li>Use the Coalesced hashing technique. This technique uses the concept of Open Addressing to find first empty place for colliding element by using the quadratic probing and the concept of Separate Chaining to link the colliding elements to each other through pointers (indices in the table). The deletion of a key is performed by linking its next entry to the entry that points the deleted key by replacing deleted entry by the next entry. See the following illustration as an example:</li>

</ul>

Input = {3, 12, 13, 25, 23, 51, 42}

Hash function = data % 10

Insert 3:                                                   insert 12:                                          insert 13:

<table width="553">

 <tbody>

  <tr>

   <td width="62">Hash Value</td>

   <td width="56">Key</td>

   <td width="64">Next</td>

   <td width="62">Hash Value</td>

   <td width="62">Key</td>

   <td width="62">Next</td>

   <td width="62">Hash Value</td>

   <td width="62">Key</td>

   <td width="62">Next</td>

  </tr>

  <tr>

   <td width="62">0</td>

   <td width="56"> </td>

   <td width="64">NULL</td>

   <td width="62">0</td>

   <td width="62"> </td>

   <td width="62">NULL</td>

   <td width="62">0</td>

   <td width="62"> </td>

   <td width="62">NULL</td>

  </tr>

  <tr>

   <td width="62">1</td>

   <td width="56"> </td>

   <td width="64">NULL</td>

   <td width="62">1</td>

   <td width="62"> </td>

   <td width="62">NULL</td>

   <td width="62">1</td>

   <td width="62"> </td>

   <td width="62">NULL</td>

  </tr>

  <tr>

   <td width="62">2</td>

   <td width="56"> </td>

   <td width="64">NULL</td>

   <td width="62">2</td>

   <td width="62">12</td>

   <td width="62">NULL</td>

   <td width="62">2</td>

   <td width="62">12</td>

   <td width="62">NULL</td>

  </tr>

  <tr>

   <td width="62">3</td>

   <td width="56">3</td>

   <td width="64">NULL</td>

   <td width="62">3</td>

   <td width="62">3</td>

   <td width="62">NULL</td>

   <td width="62">3</td>

   <td width="62">3</td>

   <td width="62">4</td>

  </tr>

  <tr>

   <td width="62">4</td>

   <td width="56"> </td>

   <td width="64">NULL</td>

   <td width="62">4</td>

   <td width="62"> </td>

   <td width="62">NULL</td>

   <td width="62">4</td>

   <td width="62">13</td>

   <td width="62">NULL</td>

  </tr>

  <tr>

   <td width="62">5</td>

   <td width="56"> </td>

   <td width="64">NULL</td>

   <td width="62">5</td>

   <td width="62"> </td>

   <td width="62">NULL</td>

   <td width="62">5</td>

   <td width="62"> </td>

   <td width="62">NULL</td>

  </tr>

  <tr>

   <td width="62">6</td>

   <td width="56"> </td>

   <td width="64">NULL</td>

   <td width="62">6</td>

   <td width="62"> </td>

   <td width="62">NULL</td>

   <td width="62">6</td>

   <td width="62"> </td>

   <td width="62">NULL</td>

  </tr>

  <tr>

   <td width="62">7</td>

   <td width="56"> </td>

   <td width="64">NULL</td>

   <td width="62">7</td>

   <td width="62"> </td>

   <td width="62">NULL</td>

   <td width="62">7</td>

   <td width="62"> </td>

   <td width="62">NULL</td>

  </tr>

  <tr>

   <td width="62">8</td>

   <td width="56"> </td>

   <td width="64">NULL</td>

   <td width="62">8</td>

   <td width="62"> </td>

   <td width="62">NULL</td>

   <td width="62">8</td>

   <td width="62"> </td>

   <td width="62">NULL</td>

  </tr>

  <tr>

   <td width="62">9</td>

   <td width="56"> </td>

   <td width="64">NULL</td>

   <td width="62">9</td>

   <td width="62"> </td>

   <td width="62">NULL</td>

   <td width="62">9</td>

   <td width="62"> </td>

   <td width="62">NULL</td>

  </tr>

 </tbody>

</table>




Insert 25:                                                 insert 23:                                          insert 51:

<table width="553">

 <tbody>

  <tr>

   <td width="62">Hash Value</td>

   <td width="56">Key</td>

   <td width="64">Next</td>

   <td width="62">Hash Value</td>

   <td width="62">Key</td>

   <td width="62">Next</td>

   <td width="62">Hash Value</td>

   <td width="62">Key</td>

   <td width="62">Next</td>

  </tr>

  <tr>

   <td width="62">0</td>

   <td width="56"> </td>

   <td width="64">NULL</td>

   <td width="62">0</td>

   <td width="62"> </td>

   <td width="62">NULL</td>

   <td width="62">0</td>

   <td width="62"> </td>

   <td width="62">NULL</td>

  </tr>

  <tr>

   <td width="62">1</td>

   <td width="56"> </td>

   <td width="64">NULL</td>

   <td width="62">1</td>

   <td width="62"> </td>

   <td width="62">NULL</td>

   <td width="62">1</td>

   <td width="62">51</td>

   <td width="62">NULL</td>

  </tr>

  <tr>

   <td width="62">2</td>

   <td width="56">12</td>

   <td width="64">NULL</td>

   <td width="62">2</td>

   <td width="62">12</td>

   <td width="62">NULL</td>

   <td width="62">2</td>

   <td width="62">12</td>

   <td width="62">NULL</td>

  </tr>

  <tr>

   <td width="62">3</td>

   <td width="56">3</td>

   <td width="64">4</td>

   <td width="62">3</td>

   <td width="62">3</td>

   <td width="62">4</td>

   <td width="62">3</td>

   <td width="62">3</td>

   <td width="62">4</td>

  </tr>

  <tr>

   <td width="62">4</td>

   <td width="56">13</td>

   <td width="64">NULL</td>

   <td width="62">4</td>

   <td width="62">13</td>

   <td width="62">7</td>

   <td width="62">4</td>

   <td width="62">13</td>

   <td width="62">7</td>

  </tr>

  <tr>

   <td width="62">5</td>

   <td width="56">25</td>

   <td width="64">NULL</td>

   <td width="62">5</td>

   <td width="62">25</td>

   <td width="62">NULL</td>

   <td width="62">5</td>

   <td width="62">25</td>

   <td width="62">NULL</td>

  </tr>

  <tr>

   <td width="62">6</td>

   <td width="56"> </td>

   <td width="64">NULL</td>

   <td width="62">6</td>

   <td width="62"> </td>

   <td width="62">NULL</td>

   <td width="62">6</td>

   <td width="62"> </td>

   <td width="62">NULL</td>

  </tr>

  <tr>

   <td width="62">7</td>

   <td width="56"> </td>

   <td width="64">NULL</td>

   <td width="62">7</td>

   <td width="62">23</td>

   <td width="62">NULL</td>

   <td width="62">7</td>

   <td width="62">23</td>

   <td width="62">NULL</td>

  </tr>

  <tr>

   <td width="62">8</td>

   <td width="56"> </td>

   <td width="64">NULL</td>

   <td width="62">8</td>

   <td width="62"> </td>

   <td width="62">NULL</td>

   <td width="62">8</td>

   <td width="62"> </td>

   <td width="62">NULL</td>

  </tr>

  <tr>

   <td width="62">9</td>

   <td width="56"> </td>

   <td width="64">NULL</td>

   <td width="62">9</td>

   <td width="62"> </td>

   <td width="62">NULL</td>

   <td width="62">9</td>

   <td width="62"> </td>

   <td width="62">NULL</td>

  </tr>

 </tbody>

</table>













Insert 42:

<table width="182">

 <tbody>

  <tr>

   <td width="62">Hash Value</td>

   <td width="56">Key</td>

   <td width="64">Next</td>

  </tr>

  <tr>

   <td width="62">0</td>

   <td width="56"> </td>

   <td width="64">NULL</td>

  </tr>

  <tr>

   <td width="62">1</td>

   <td width="56">51</td>

   <td width="64">NULL</td>

  </tr>

  <tr>

   <td width="62">2</td>

   <td width="56">12</td>

   <td width="64">6</td>

  </tr>

  <tr>

   <td width="62">3</td>

   <td width="56">3</td>

   <td width="64">4</td>

  </tr>

  <tr>

   <td width="62">4</td>

   <td width="56">13</td>

   <td width="64">7</td>

  </tr>

  <tr>

   <td width="62">5</td>

   <td width="56">25</td>

   <td width="64">NULL</td>

  </tr>

  <tr>

   <td width="62">6</td>

   <td width="56">42</td>

   <td width="64">NULL</td>

  </tr>

  <tr>

   <td width="62">7</td>

   <td width="56">23</td>

   <td width="64">NULL</td>

  </tr>

  <tr>

   <td width="62">8</td>

   <td width="56"> </td>

   <td width="64">NULL</td>

  </tr>

  <tr>

   <td width="62">9</td>

   <td width="56"> </td>

   <td width="64">NULL</td>

  </tr>

 </tbody>

</table>




Delete 13:

<table width="182">

 <tbody>

  <tr>

   <td width="62">Hash Value</td>

   <td width="56">Key</td>

   <td width="64">Next</td>

  </tr>

  <tr>

   <td width="62">0</td>

   <td width="56"> </td>

   <td width="64">NULL</td>

  </tr>

  <tr>

   <td width="62">1</td>

   <td width="56">51</td>

   <td width="64">NULL</td>

  </tr>

  <tr>

   <td width="62">2</td>

   <td width="56">12</td>

   <td width="64">6</td>

  </tr>

  <tr>

   <td width="62">3</td>

   <td width="56">3</td>

   <td width="64">4</td>

  </tr>

  <tr>

   <td width="62">4</td>

   <td width="56">23</td>

   <td width="64">NULL</td>

  </tr>

  <tr>

   <td width="62">5</td>

   <td width="56">25</td>

   <td width="64">NULL</td>

  </tr>

  <tr>

   <td width="62">6</td>

   <td width="56">42</td>

   <td width="64">NULL</td>

  </tr>

  <tr>

   <td width="62">7</td>

   <td width="56"> </td>

   <td width="64">NULL</td>

  </tr>

  <tr>

   <td width="62">8</td>

   <td width="56"> </td>

   <td width="64">NULL</td>

  </tr>

  <tr>

   <td width="62">9</td>

   <td width="56"> </td>

   <td width="64">NULL</td>

  </tr>

 </tbody>

</table>




Test all the three hash table implementations empirically. Use small, medium, and large-sized data and hash tables in suitable sizes for testing. Perform different tasks over the tables to compare their performance results (like accessing existing/non-existing items or adding/removing items).