Download Link: https://assignmentchef.com/product/solved-ccu-oop-homework-5-overloading-bigint-myvector
<br>
<strong>HW #5 </strong><strong>(Overloading: BigInt &amp; MyVector) </strong><strong>Part 1:</strong>

<ul>

 <li>Here we introduce a BigInt class which can represent integers much larger than the maximum bound for <em>integer </em>type in computers.</li>

 <li>You will deal with only <strong>positive </strong>BigInt in this problem. The BigInt class uses a dynamic array of <strong>char </strong>to represent the “big” integers. Each of the elements in the array can only be one of ‘0’, ‘1’, ‘2’, …, ‘9’, i.e., each array element stores just <em>one </em>digit of the “big” integer.</li>

 <li>The BigInt.h file defines the BigInt class as follows:</li>

</ul>

<strong>HW #5 </strong>

class BigInt { public:

// constructor

BigInt () {

num = NULL;

size = 0;

};

<h1>HW #5</h1>

// convert an array of integral digits by tmp to BigInt

// tmp: pointer to the array

// length: the number of digits in the array BigInt (const int* tmp, int length);

BigInt (const BigInt &amp;); // copy constructor

// Assignment

const BigInt &amp; operator=(const BigInt &amp;);




// destructor

~BigInt() { if (num != NULL) delete [ ] num;

};

char &amp; operator[ ] (int index); int length() const { return size; }; char* getNum() { return num; };

<h1>HW #5</h1>

private: char* num; // the big integer in char

int size;     // number of digits in the big integer

};

<strong>1A:</strong>

<ul>

 <li>Implement the overloading of the operator [ ], so that it returns the digits in <em>char </em>of a particular index. For example, if A is a BigInt object, we can get the 5th digit of A from the left in <em>char </em>by calling A[4] (digits are indexed 0, 1, 2, … from the left).</li>

</ul>

char &amp; BigInt::operator [ ] (int index) { assert (index &gt;=0 &amp;&amp; index &lt; size);

// your code below




<strong>1B:</strong>

<ul>

 <li>Implement the constructor which takes in an integer array of digits and converts it to a BigInt object. You may assume that the digits in the array are all integers between 0 and 9.</li>

 <li><strong>Hint: </strong>in order to convert a digits to a <em>char </em>type, you can add (‘1’ – 1) to it. For example, if you want to convert the digit 3 to a <em>char </em>in the form of ‘3’, you can use 3 + (‘1’ – 1).</li>

</ul>

// convert an integer array of digits (0-9) to BigInt

// tmp: pointer to the array

// length: the number of digits in the integer array

BigInt (const* tmp, int length) {

<strong>1C:</strong>

<ul>

 <li>In addition to the above, you need to implement prefix increment of BigInt, i.e., you want to support <em>++bi </em>for a BigInt <em>bi</em>. Write the prototype of the member function in the BigInt class, and its implementation outside the class.</li>

</ul>

<strong>1D:</strong>

<ul>

 <li>You also want to implement postfix increment which supports <em>bi++ </em>for a BigInt <em>bi</em>. Write the prototype of the member function in the BigInt class, and its implementation outside the class.</li>

</ul>

<strong>Part 2:</strong>

<ul>

 <li>Design a class MyVector with two <strong>private </strong>data members: <em>int length </em>and a <em>pointer to double </em>for memory dynamic allocation.</li>

 <li>Include the following methods in the <strong>public </strong>section:</li>

 <li>two constructors: one default without parameters and one constructor initializer with one parameter of <em>int </em>type which will be used for specifying the requested vector length, the other parameter of <em>pointer </em>type for specifying that vector.</li>

 <li>a copy constructor;</li>

</ul>




<h1>HW #5</h1>

<ul>

 <li>destructor;</li>

 <li>assignment operator;</li>

 <li>overload the output operator &lt;&lt;;</li>

 <li>operator* for calculating inner product of two vectors; • operator* for vector multiplication with a constant;</li>

 <li>operator+ for adding two vectors.</li>

 <li>Write a test program which implements all of the above methods.</li>

</ul>