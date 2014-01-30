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

`#count`

`#cycle`

`#detect`

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