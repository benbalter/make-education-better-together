---
excerpt: ""
---

{% highlight php %}
<?php
/**
 * Recursively merges and sorts an array
 * @param array $array the unsorted array
 * @returns array the sorted array
 */
function bb_merge_sort( $array ) {
  
  //if array is but one element, array is sorted, so return as is
  if ( sizeof ( $array ) <= 1 )
          return $array;

  //bifurcate unsorted array
  $array2 = array_splice( $array, ( sizeof( $array ) / 2 ) );

  //recursively merge-sort and return
  return bb_merge( bb_merge_sort( $array ), bb_merge_sort( $array2 ) );
  
}
{% endhighlight %}
