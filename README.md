Download Link: https://assignmentchef.com/product/solved-comp2210-assignment1-array-selector
<br>
This assignment focuses on implementing the methods of a class much like <sub>java.util.Arrays</sub>. The Selector.java file defines a class with static methods designed to provide useful functionality on arrays. Each method of <sub>Selector </sub>is very clearly specified, is independent of the other methods in the class, and is designed to provide relatively simple functionality. So, this is a great context for practicing what we are discussing in lecture – systematic, disciplined development and test-based verification.

<h1>The Selector class</h1>

You must correctly implement all the method bodies of the provided <sub>Selector </sub>class. Your implementation must adhere <em><sub>exactly </sub></em>to the API of the <sub>Selector </sub>class, as described in the provided source code comments and as described below.

public final class Selector { public static int    min(int[] a) public static int         max(int[] a) public static int               kmin(int[] a, int k) public static int         kmax(int[] a, int k) public static int[] range(int[] a, int low, int high) public static int    ceiling(int[] a, int key) public static int            floor(int[] a, int key)

}

<strong>The min method.</strong>

This method selects the minimum value from a given array. If the array is null or has zero length, this method throws an IllegalArgumentException. The array is not changed by this method.

<em>Examples:</em>

<table width="174">

 <tbody>

  <tr>

   <td width="126">a[ ]</td>

   <td width="47">min(a)</td>

  </tr>

  <tr>

   <td width="126">[2, 8, 7, 3, 4]</td>

   <td width="47">2</td>

  </tr>

  <tr>

   <td width="126">[5, 9, 1, 7, 3]</td>

   <td width="47">1</td>

  </tr>

  <tr>

   <td width="126">[8, 7, 6, 5, 4]</td>

   <td width="47">4</td>

  </tr>

  <tr>

   <td width="126">[2, 8, 8, 7, 3, 3, 4]</td>

   <td width="47">2</td>

  </tr>

 </tbody>

</table>

<strong>The max method.</strong>

This method selects the maximum value from a given array. If the array is null or has zero length, this method throws an IllegalArgumentException. The array is not changed by this method.

1

<em>Examples:</em>

<table width="176">

 <tbody>

  <tr>

   <td width="126">a[ ]</td>

   <td width="50">max(a)</td>

  </tr>

  <tr>

   <td width="126">[2, 8, 7, 3, 4]</td>

   <td width="50">8</td>

  </tr>

  <tr>

   <td width="126">[5, 9, 1, 7, 3]</td>

   <td width="50">9</td>

  </tr>

  <tr>

   <td width="126">[8, 7, 6, 5, 4]</td>

   <td width="50">8</td>

  </tr>

  <tr>

   <td width="126">[2, 8, 8, 7, 3, 3, 4]</td>

   <td width="50">8</td>

  </tr>

 </tbody>

</table>

<strong>The kmin method.</strong>

This method selects the <em><sub>k</sub><sup>th </sup></em>minimum value from a given array. A value is the <em><sub>k</sub><sup>th </sup></em>minimum if there are exactly <em><sub>k − </sub></em>1 values less than it in the array. If the array is null, has zero length, or if there is no <em><sub>k</sub><sup>th </sup></em>minimum value, this method throws an IllegalArgumentException. Note that there is no <em><sub>k</sub><sup>th </sup></em>minimum value if <em><sub>k </sub></em>is less than 1, <em><sub>k </sub></em>is greater than the number of elements in the array, or if <em><sub>k </sub></em>is greater than the number of distinct values in the array. The array is not changed by this method.

<em>Examples:</em>

<table width="219">

 <tbody>

  <tr>

   <td width="126">a[ ]</td>

   <td width="23">k</td>

   <td width="69">kmin(a, k)</td>

  </tr>

  <tr>

   <td width="126">[2, 8, 7, 3, 4]</td>

   <td width="23">1</td>

   <td width="69">2</td>

  </tr>

  <tr>

   <td width="126">[5, 9, 1, 7, 3]</td>

   <td width="23">3</td>

   <td width="69">5</td>

  </tr>

  <tr>

   <td width="126">[8, 7, 6, 5, 4]</td>

   <td width="23">5</td>

   <td width="69">8</td>

  </tr>

  <tr>

   <td width="126">[2, 8, 8, 7, 3, 3, 4]</td>

   <td width="23">3</td>

   <td width="69">4</td>

  </tr>

 </tbody>

</table>

<strong>The kmax method.</strong>

This method selects the <em><sub>k</sub><sup>th </sup></em>maximum value from a given array. A value is the <em><sub>k</sub><sup>th </sup></em>maximum if there are exactly <em><sub>k − </sub></em>1 values greater than it in the array. If the array is null, has zero length, or if there is no <em><sub>k</sub><sup>th </sup></em>maximum value, this method throws an IllegalArgumentException. Note that there is no <em><sub>k</sub><sup>th </sup></em>maximum value if <em><sub>k </sub></em>is less than 1, <em><sub>k </sub></em>is greater than the number of elements in the array, or if <em><sub>k </sub></em>is greater than the number of distinct values in the array. The array is not changed by this method.

<em>Examples:</em>

<table width="221">

 <tbody>

  <tr>

   <td width="126">a[ ]</td>

   <td width="23">k</td>

   <td width="72">kmax(a, k)</td>

  </tr>

  <tr>

   <td width="126">[2, 8, 7, 3, 4]</td>

   <td width="23">1</td>

   <td width="72">8</td>

  </tr>

  <tr>

   <td width="126">[5, 9, 1, 7, 3]</td>

   <td width="23">3</td>

   <td width="72">5</td>

  </tr>

  <tr>

   <td width="126">[8, 7, 6, 5, 4]</td>

   <td width="23">5</td>

   <td width="72">4</td>

  </tr>

  <tr>

   <td width="126">[2, 8, 8, 7, 3, 3, 4]</td>

   <td width="23">3</td>

   <td width="72">4</td>

  </tr>

 </tbody>

</table>

<strong>The range method.</strong>

This method returns an array of all values <em><sub>i </sub></em>from a given array such that <em><sub>low ≤ i ≤ high</sub></em>, including duplicate values. (Note that <em><sub>low </sub></em>and <em><sub>high </sub></em>do not have to be actual values in the given array, and the order of the resulting values is irrelevant.) The length of the returned array is the same as the number of values <em><sub>i </sub></em>that meet the criterion. If there are no values <em><sub>i </sub></em>that meet the criterion, this method returns a zero-length array. If the given array is null or has zero length, this method throws an IllegalArgumentException. The given array is not changed by this method.

<em>Examples:</em>

<em>Page 2 of 3</em>

<table width="321">

 <tbody>

  <tr>

   <td width="126">a[ ]</td>

   <td width="35">low</td>

   <td width="41">high</td>

   <td width="118">range(a, low, high)</td>

  </tr>

  <tr>

   <td width="126">[2, 8, 7, 3, 4]</td>

   <td width="35">1</td>

   <td width="41">5</td>

   <td width="118">[2, 3, 4]</td>

  </tr>

  <tr>

   <td width="126">[5, 9, 1, 7, 3]</td>

   <td width="35">3</td>

   <td width="41">5</td>

   <td width="118">[3, 5]</td>

  </tr>

  <tr>

   <td width="126">[8, 7, 6, 5, 4]</td>

   <td width="35">4</td>

   <td width="41">8</td>

   <td width="118">[8, 7, 6, 5, 4]</td>

  </tr>

  <tr>

   <td width="126">[2, 8, 8, 7, 3, 3, 4]</td>

   <td width="35">3</td>

   <td width="41">7</td>

   <td width="118">[7, 3, 3, 4]</td>

  </tr>

 </tbody>

</table>

<strong>The ceiling method.</strong>

This method returns the smallest value <em><sub>i </sub></em>in a given array such that <em><sub>i ≥ key</sub></em>. (Note that <em><sub>key </sub></em>does not have to be an actual value in the given array.) If the given array is null or has zero length, or if there is no qualifying value <em><sub>i</sub></em>, this method returns an IllegalArgumentException. The given array is not changed by this method.

<em>Examples:</em>

<table width="252">

 <tbody>

  <tr>

   <td width="126">a[ ]</td>

   <td width="35">key</td>

   <td width="90">ceiling(a, key)</td>

  </tr>

  <tr>

   <td width="126">[2, 8, 7, 3, 4]</td>

   <td width="35">1</td>

   <td width="90">2</td>

  </tr>

  <tr>

   <td width="126">[5, 9, 1, 7, 3]</td>

   <td width="35">7</td>

   <td width="90">7</td>

  </tr>

  <tr>

   <td width="126">[8, 7, 6, 5, 4]</td>

   <td width="35">0</td>

   <td width="90">4</td>

  </tr>

  <tr>

   <td width="126">[2, 8, 8, 7, 3, 3, 4]</td>

   <td width="35">5</td>

   <td width="90">7</td>

  </tr>

 </tbody>

</table>

<strong>The floor method.</strong>

This method returns the largest value <em><sub>i </sub></em>in a given array such that <em><sub>i ≤ key</sub></em>. (Note that <em><sub>key </sub></em>does not have to be an actual value in the given array.) If the given array is null or has zero length, or if there is no qualifying value <em><sub>i</sub></em>, this method returns an IllegalArgumentException. The given array is not changed by this method.

<em>Examples:</em>

<table width="241">

 <tbody>

  <tr>

   <td width="126">a[ ]</td>

   <td width="35">key</td>

   <td width="79">floor(a, key)</td>

  </tr>

  <tr>

   <td width="126">[2, 8, 7, 3, 4]</td>

   <td width="35">6</td>

   <td width="79">4</td>

  </tr>

  <tr>

   <td width="126">[5, 9, 1, 7, 3]</td>

   <td width="35">1</td>

   <td width="79">1</td>

  </tr>

  <tr>

   <td width="126">[8, 7, 6, 5, 4]</td>

   <td width="35">9</td>

   <td width="79">8</td>

  </tr>

  <tr>

   <td width="126">[2, 8, 8, 7, 3, 3, 4]</td>

   <td width="35">5</td>

   <td width="79">4</td>

  </tr>

 </tbody>

</table>


