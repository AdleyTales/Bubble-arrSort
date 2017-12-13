# 封装自己JS 的冒泡排序方法 arrSort

```js

    <!DOCTYPE html>
    <html>
      <head>
        <meta charset="utf-8">
        <title>js冒泡排序</title>
      </head>
      <body>

        <script type="text/javascript">
          // 数组的排序
          // 升序：从小到大  降序：从大到小

          /**
           * 经典排序：冒泡排序 升序
           *
           * 原理： 依次比较相邻的两个值，如果后面的比前面的小，则将小的元素排到前面。
           * 依照这个规则进行多次并且递减的迭代，直到顺序正确。
           *
           */

          var arrSort = arrSort || {};

          //  升序
          arrSort.up = function(arr){
            // 比较次数
            for(var i=0;i<arr.length-1;i++){
              // 每次比较
              for(var j=0;j<arr.length -1 -i;j++){
                if(arr[j] > arr[j+1]){
                  var temp = arr[j];
                  arr[j] = arr[j+1];
                  arr[j+1] = temp;
                }
              }
            }
            return arr;
          }

          //  降序
          arrSort.down = function(arr){
            // 比较次数
            for(var i=0;i<arr.length-1;i++){
              // 每次比较
              for(var j=0;j<arr.length -1 -i;j++){
                if(arr[j] < arr[j+1]){
                  var temp = arr[j];
                  arr[j] = arr[j+1];
                  arr[j+1] = temp;
                }
              }
            }
            return arr;
          }

          var arr = [12,3,43,54,33,2,32,23,23,2,3,2,3,23,4,2,3,2,3,2,3,2,66,32];
          console.log(arrSort.up(arr));
          console.log(arrSort.down(arr));

        </script>
      </body>
    </html>


```
