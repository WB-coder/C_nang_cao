# C_C++_Advanced
contains all materials and descriptions of the C and C++ advanced course
(https://drive.google.com/drive/folders/1jjzoKAvMiv9q1zVPqWuDF5aCdYt7LtzL?usp=drive_link)




**Lesson 9 (Pointer):**

_ Initialize a pointer: 

    int *ptr1 = NULL;

    float *ptr2 = &a;

    void *ptr = &b;

_ Initialize a pointer in function:

    int sum (int *a, int *b)
    {
        return *a + *b;
    }
_ Function pointer:

    int sum (int *a, int *b)
    {
        return *a + *b;
    }
    
    int product (int *a, int *b)
    {
        return *a * *b;
    }
    
    int calculate (int *a, int *b, int (*ptr) (int,int))
    {
        return ptr(a,b);
    }
    int main()
    {
        calculate(9,6, &sum);
    }
    // The answer will be 15
_ Void pointer:
    
    /*
    It is impossible to point more variable address which have different types. 
    Therefore, void pointer help to point any type of variable, but still need type conversion to get the variable value.
    */
    int main()
    {
        int a;
        float b;
        char c;
        void *ptr = &a;
        ptr = &b;
        ptr = &c;
        // print the value and the address of c variable
        printf("ptr points to value: %d\n ptr storing address: %p", *(char*)ptr, ptr);
    }
