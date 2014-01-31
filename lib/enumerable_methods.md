#####*Descriptions to follow...*

`#all?` *passes each element to the block and it returns true if no false or nil occurs within the block. This would be used the way I see it, to check whether each of the values meets a certain condition specified in the block `[1,2,3,4,5].all? { |x| x.is_a?(Fixnum) } --> true`.* 
*Similar example returning false `[1,2,3,4,'5'].all? { |x| x.is_a?(Fixnum) } --> false, since '5' is not a Fixnum.`.*

`#any?` *passes each element to the block and checks to say whether any of the elements meets the condition in the block. If it does it returns true. Taking the example from above `[1,2,3,4,'5'].any { |x| x.is_a?(String) } --> true`*

`#chunk` *this one looks like it needs ALOT of playing around with. Will return back to it.*

`#collect` *returns a new array with the result of running the block once for each element in the enum.*
*i.e `a = [1,2,3,4,5]` then `f = a.collect { |x| "Kowabunga #{x}!" }` will set the value of f to:* 
*`['Kowabunga 1!','Kowabunga 2!','Kowabunga 3!','Kowabunga 4!','Kowabunga 5!']`*
*__Note__: using a bang(!) will alter the original array thus wont return a new array.*
*Doing the same as above but with a !: `a.collect! { |x| "Kowabunga #{x}!" }` will make a:*
*`['Kowabunga 1!','Kowabunga 2!','Kowabunga 3!','Kowabunga 4!','Kowabunga 5!']`*

`#collect_concat` *__Note__: same thing as __flat_map__ method. Returns a new array with the concatenated results of running block once for each element. In other words if you do this: `[1,2,3,4,5].collect_concat { |x| 100 + x }` it will return: `[101,102,103,104,105]`*

`#count` *This one returns the number of items in an enum: `[1,2,3,4,5].count --> 5`*
*If passed an argument it will scan the enum and return the number of times the argument appears:* 
*`[1,2,1,3,4].count(1) --> 2`. This works with other types of data too: `['hi',1,2,'hi',3,'hi'].count('hi') --> 3`*
*It can also be passed a block: `[1,2,3,4,5].count { |x| x > 4 } --> 1`, in this case returning amount of instances that match the condition, only 5 is greater than 4, thus 1 instance.*

`#cycle` *This is quite interesting. With cycle you essentially call a block a x amount of times or let it run forever if you feel adventurous or just bored. So things like this are possible `[1,2,3,4,5].cycle(2) { |x| puts x } --> 1, 2, 3, 4, 5, 1, 2, 3, 4, 5`. If run it without the parameter (2) it will keep running forever. This can be useful when you create an object that will return the next value in a repeating sequence:*
*`heroes = ['captain america', 'thor', 'iron man', 'black panther'].cycle`*
*`heroes.next --> 'captain america'` or do some chaining: `heroes.next.upcase --> 'THOR'`*
*__Note__: Once you reach the end of the array it will start from the beginning again.*
*A cool thing you can do is say you're in the middle: `heroes.next --> 'thor'` and suddenly you decide you want to start from the beginning of the array, you can call `rewind`: `heroes.rewind` and it will reset the enumerator to start from the beginning.*

`#detect` *__Note__: `detect` and `find` do the same thing. It returns the first value that meets the criteria: `(1..20).detect { |x| x > 9 } --> 10`. If no value matches the criteria it will return nil: `(1..20).detect { |x| x > 100 } --> nil`*
*You can pass `detect` and argument which will be either a lambda or a Proc and which will be called if no value matches the conditions:*
`number = Proc.new do`
                    `n = [101]`
                    `"#{n} is a good example!"`
`(1..20).detect(number) { |x| x > 100} --> "101 is a good example!"`
*In the above case detect after seeing that not value meets the criteria, proceeds to call the number proc in this case which returns it's value.*

`#drop`

`#drop_while`


`#each_cons`

`#each_entry`

`#each_slice`

`#each_with_index`

`#each_with_object`

`#entries`

`#find`

`#find_all`


`#find_index`

`#first`

`#flat_map`

`#grep`

`#group_by`

`#include?`

`#inject`

`#lazy`

`#map`

`#max`

`#max_by`

`#member?`

`#min`

`#min_by`

`#minmax`

`#minmax_by`

`#none?`

`#one?`

`#partition`

`#reduce`

`#reject`

`#reverse_each`

`#select`

`#slice_before`

`#sort`

`#sort_by`

`#take`

`#take_while`

`#to_a`

`#to_h`

`#zip`