# 排序算法

常见排序算法如下:

<div align=center><img width="700" src="figure/1.png" alt=" "/></div>

## 冒泡排序

* 比较相邻的元素. 如果第一个比第二个大, 就交换它们两个.
* 对每一对相邻元素作同样的工作, 从开始第一对到结尾的最后一对, 这样在最后的元素应该会是最大的数.
* 针对所有的元素重复以上的步骤, 除了最后一个.
* 重复步骤1~3, 直到排序完成.

<div align=center><img width="700" src="figure/2.gif" alt=" "/></div>

## 选择排序

* 首先在未排序序列中找到最小元素, 存放到排序序列的起始位置.
* 再从剩余未排序元素中继续寻找最小元素, 然后放到已排序序列的末尾.
* 重复第二步, 直到所有元素均排序完毕.

<div align=center><img width="700" src="figure/3.gif" alt=" "/></div>

## 插入排序

* 从第一个元素开始, 该元素可以认为已经被排序.
* 取出下一个元素, 在已经排序的元素序列中从后向前扫描.
* 如果该元素(已排序)大于新元素, 将该元素移到下一位置.
* 重复步骤3, 直到找到已排序的元素小于或者等于新元素的位置.
* 将新元素插入到该位置后.
* 重复步骤2~5.

<div align=center><img width="700" src="figure/4.gif" alt=" "/></div>

## 希尔排序(缩小增量排序)

* 选择一个增量序列t1, t2, ... , tk, tk = 1.
* 按增量序列个数k, 对序列进行k趟排序.
* 每趟排序, 根据对应的增量ti, 将待排序列分割成若干长度为m的子序列, 分别对各子表进行直接插入排序.
* 仅增量因子为1时, 整个序列作为一个表来处理, 表长度即为整个序列的长度.

<div align=center><img width="700" src="figure/5.gif" alt=" "/></div>

## 归并排序

* 把长度为n的输入序列分成两个长度为n/2的子序列.
* 对这两个子序列分别采用归并排序.
* 将两个排序好的子序列合并成一个最终的排序序列.

<div align=center><img width="700" src="figure/6.gif" alt=" "/></div>

## 快速排序

* 从数列中挑出一个元素, 作为基准.
* 重新排序数列, 所有元素比基准值小的摆放在基准前面, 所有元素比基准值大的摆在基准的后面(相同的数可以到任一边). 在这个分区退出之后, 该基准就处于数列的中间位置, 称为分区操作.
* 递归地把小于基准值元素的子数列和大于基准值元素的子数列排序.

<div align=center><img width="700" src="figure/7.gif" alt=" "/></div>

## 堆排序

* 将初始待排序关键字序列(R1, R2, ... , Rn)构建成大顶堆, 此堆为初始的无序区.
* 将堆顶元素R[1]与最后一个元素R[n]交换, 此时得到新的无序区(R1, R2, ... , Rn-1)和新的有序区(Rn), 且满足R[1, 2 , ... , n-1]<=R[n]；
* 由于交换后新的堆顶R[1]可能违反堆的性质, 因此需要对当前无序区(R1, R2, ... , Rn-1)调整为新堆, 然后再次将R[1]与无序区最后一个元素交换, 得到新的无序区(R1, R2, ... ,Rn-2)和新的有序区(Rn-1, Rn).
* 不断重复此过程直到有序区的元素个数为n-1, 则整个排序过程完成.

<div align=center><img width="700" src="figure/8.gif" alt=" "/></div>

## 计数排序

* 找出待排序的数组中最大和最小的元素.
* 统计数组中每个值为i的元素出现的次数, 存入数组C的第i项.
* 对所有的计数累加(从C中的第一个元素开始, 每一项和前一项相加).
* 反向填充目标数组: 将每个元素i放在新数组的第C(i)项, 每放一个元素就将C(i)减去1.

<div align=center><img width="700" src="figure/9.gif" alt=" "/></div>

## 桶排序

* 设置一个定量的数组当作空桶.
* 遍历输入数据, 并且把数据一个一个放到对应的桶里去.
* 对每个不是空的桶进行排序.
* 从不是空的桶里把排好序的数据拼接起来.

<div align=center><img width="700" src="figure/10.gif" alt=" "/></div>

## 基数排序

* 取得数组中的最大数, 并取得位数.
* arr为原始数组, 从最低位开始取每个位组成radix数组.
* 对radix进行计数排序(利用计数排序适用于小范围数的特点).

<div align=center><img width="700" src="figure/11.gif" alt=" "/></div>