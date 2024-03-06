/**

 * Note: The returned array must be malloced, assume caller calls free().

 */
int* buildArray(int* nums, int numsSize, int* returnSize) {
    int *arr = malloc(numsSize*sizeof(int)); // 分配一個與原陣列相同大小的記憶體
    *returnSize = numsSize; // 回傳新陣列的長度

    for(int i = 0; i < numsSize; i++){ // 利用for迴圈反覆執行
        *(arr + i) = *(nums + *(nums + i)); //題目內容
    }

    return arr; // 回傳陣列(指標)
}
