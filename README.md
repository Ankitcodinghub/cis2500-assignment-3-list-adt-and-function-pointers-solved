# cis2500-assignment-3-list-adt-and-function-pointers-solved
**TO GET THIS SOLUTION VISIT:** [CIS2500 Assignment 3-List ADT and Function Pointers Solved](https://www.ankitcodinghub.com/product/cis2500-question-1b-list-adt-and-function-pointers-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;115162&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CIS2500 Assignment 3-List ADT and Function Pointers Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
Using the same data type Sorted_List as in q1a,

Implement

• Sorted_List * map ( Sorted_List *, fn ptr) o map only applies to the values, not the sort keys

o however, make sure that the new list produced has the same key values and links (both next and sort)

• value_type reduce ( Sorted_List *, reduce fn ptr, value_type init, int order ) o like map, reduce only applies to values, not keys

o however, reduce also takes an extra parameter, int order

§ order is either INSERTED_ORDER or SORTED_ORDER and determines which set of links to follow while reducing: next or sort respectively

§ note: while the order of the reduction does not matter when using add or mult as the reducing function, it could with other reduction functions

• value_type map_reduce ( Sorted_List *list, map fn ptr, reduce fn ptr, value_type init, int order )

o Conceptually, you are first applying map, and then reduce

o However, both map_fn and reduce_fn should be applied together, node-by-node

§ i.e. do not create a full map list and then apply reduce to it

§ instead apply the map function to list’s node, then store the result in the reduce accumulator

o This allows you to avoid creating and freeing the memory that would be used if an intermediate map list were to have been created and only then reduced

• value_type * map_2_array ( Sorted_List *list1, List_Sort *list2, fn ptr, int order ) o map_2_array takes two lists and applies a function, passed in as a function pointer, that takes two values (from the nodes at the same position in their respective lists) and returns a value of type value_type

o The values are collected in an array with element type value_type in the same order as traversed along the links chosen (i.e. next if INSERTED_ORDER was chosen or sort if SORTED_ORDER was)

o the function then returns the above array

note: unlike map, order of traversal matters with map_2_array as different nodes will be paired together depending on the order

• value_type map_2_reduce( Sorted_List *list1, List_Sort *list2, map fptr, reduce fptr, value_type init, int order ) o Similar to map_reduce,

o However, node by node, it should

§ apply the map function to the value of list1’s node as its first argument and the value of list2’s node as its second argument

§ then store the result in reduce’s accumulator

Below list1 and list2 only depict the value and next fields

Figure 1: Example of map_2array and map_2_reduce using INSERTED_ORDER

list1 and list2 are the same as before,  but now depict the key and sort fields where key was set equal to value

Figure 2: Example of map_2array and map_2_reduce using SORTED_ORDER

To test within, map, reduce, etc.

Write a program called a4q1b.c

• Data types used

o value_type datatype is equal to int o key_type datatype is equal to double o same as a4q1a_int.c, so compile files containing Sorted_List functions using -DINT

• The program reads in a text file that contains a series of commands, one per line, with the name of the text file entered as a command line argument o Base this code on the code you used in q1a to implement command entries from a file o However, the code will need to be extended to allow for new commands that are detailed below

• Again, all commands are echoed to stdout, followed by a colon : in the same format as used with q1

• Include a void print_array(value_type *, int size) o this prints out values in the array produced by map_2_array

o the values in the array should be printed one per line, with five spaces preceding the value

• Make sure you have declared an array that can hold up to 10 Sorted_List pointers o Do not confuse this with the array produced by map_2_array, this array holds Sorted_List pointers not value_type values.

To implement the new commands, write the following functions use either map, reduce, map_reduce, map_2_array, or map_2_reduce when implementing

• sum

• diff o takes two sorted lists of the same size

 returns FAILURE or NULL if the sizes are different (depending on how you design the function) o produces an array whose values are the differences of the values in the sorted lists args o you should also take a third argument that can be set to SORTED_ORDER or INSERTED_ORDER in order to follow the appropriate links

• square o takes a sorted list and produces a new sorted list whose value at a node equals the original value (not key) squared

o the keys and links should be copied unchanged

• sum_of_sq_diff o takes two sorted lists of the same size

§ returns a value to indicate failure if the sizes are different o produces a value computed as follows:

§ at each node position, take the difference between the values

§ square the resulting difference

§ sum across all nodes into a single result o you should also take a third argument that can be set to SORTED_ORDER or INSERTED_ORDER in order to follow the appropriate links

note 1: these should be 1 or 2 line programs that take function pointers to functions that are also only a few lines long

List of Commands

All commands from q1a should be made available as well as the following

Silent Commands (modifies the list but does not print anything other than the command itself)

• a|n key value

o append to the nth index of the array of sorted list pointers that you have set up for the program to use (see the 5th point on how to set up the program two pages back)

o same as the a command but appends the key/value pair into the array of sorted lists

• p|n key value

o same as a|n except it pushes instead of appends the key/value pair into the array of sorted lists

Report Commands (prints information, but does not modify the list)

For all examples, the sorted list at index 3 holds the values &lt;1, 2, 3&gt; where the key equals the value the sorted list at index 5 holds the values &lt;3, 1, 7&gt; where the key equals the value

• print_all|n

o print the sorted list at index n in insertion order

o Using the input from the append examples in q1a that had been stored at index 2

For the command “print_all|2”, the output should be

print_all: list = 2, Insertion Order

3.27 1427

0.94 984

7.21 346

• print_sort|n

o print the sorted list at index n in key sort order

• sum|n

o sums the values of the sorted list at index n o For the command “sum|3”, the output should be sum: list = 3, result = 6

• square|n o For the command “square|3”, the output should be square: list = 3

1.0 1

2.0 4

3.0 9 o remember to free any new list produced, after it has been printing

• diff|n:m order o For the command “diff|5:3 INSERTED_ORDER”, the output should be diff: list1 = 5, list2 = 3, Insertion Order

2

-1

4 o remember to free any new list produced, after it has been printing

• sum_sq_d|n:m order o For the command “sum_sq_d |5:3 INSERTED_ORDER”, the output should be sum_sq_d: list = 5, list2 = 3, Insertion Order, result = 21

The assignment continues with Question 2: Recursion
