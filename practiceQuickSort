#define _CRT_SECURE_NO_WARNINGS
#include <iostream>
#include <string>
#include <vector>
#include <algorithm>
#include <time.h>
using namespace std;

void PrintArray(int array[], int len)
{
    for (int i = 0; i < len; i++)
    {
        cout << array[i] << " ";
    }
    cout << endl;
}

void quicksort(int array[], int start, int last)
{
    int i = start;
    int j = last;
    int temp = array[i];
    if (i < j)
    {
        while (i < j)
        {
            //
            while (i < j &&  array[j]>=temp )
                j--;
            if (i < j)
            {
                array[i] = array[j];
                i++;
            }

            while (i < j && temp > array[i])
                i++;
            if (i < j)
            {
                array[j] = array[i];
                j--;
            }

        }
        //把基准数放到i位置
        array[i] = temp;
        //递归方法
        quicksort(array, start, i - 1);
        quicksort(array, i + 1, last);
    }
}
int main(void)
{
    const int NUM = 10;
    int array[NUM] = { 0 };
    srand((unsigned int)time(nullptr));
    for (int i = 0; i < NUM; i++)
    {
        array[i] = rand() % 100 + 1;
    }
    cout << "before array: " << endl;
    PrintArray(array, NUM);
    cout << "after array: " << endl;
    quicksort(array, 0, NUM - 1);
    PrintArray(array, NUM);

    return 0;
}
