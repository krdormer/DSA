# Data Structures
## Arrays
1. Smallest 'footprint'
2. Organizes data sequentially in memory
    - Contiguous
3. Items are stored and accessed via a numerical index, starting at 0
    - Key/value pairs where the key is always numerical
4. Performance
    1. Access / Lookup
	* Get data at specific location in array
	* O(1) - Constant time
	* `arr[0]` => returns item at zeroth position in array
    2. Push
	* Add data to end of array
	* O(1) - Contant time
	* `arr.push('hello');` => ['hello']
    3. Unshift
	* Add data to beginning of array
	* O(n) - Linear time
	    - Since new item will be at index 0, all previous items will need to be shifted +1 index position
    4. Pop
	* Remove last item in array
	* O(1) - Constant time
	* `arr.pop();` => [] => 'hello'
    5. Splice
	* Removes an item from an array sat a specified index
	    - Optional: Can add an item if given as third argument to spliced index
	* O(n)
	* `arr.splice(startIndex, numberOfItemsToDelete, itemToReplace);`
5. Static vs. Dynamic Arrays
    1. Static Array
	* Array size, and number of items it can hold, defined at declaration of array
	* Can hold less, but never more than predefined size
	    - If more memory is needed, the array is copied into a larger array, which can then be pushed into
	* Good for memory management, and when size of items will be known
    2. Dynamic Array
	* JS
	* When an array is defined, it is given an automatic amount of space
	    - 64 bits
	* If more memory is needed, the array is copied, doubled in size, and then can accept new items 
