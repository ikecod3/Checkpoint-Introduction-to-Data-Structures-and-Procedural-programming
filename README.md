# Checkpoint-Introduction-to-Data-Structures-and-Procedural-programming

## PROBLEM 1
# Algorithm to find the sum of all distinct elements from the set. In other words, find the sum of all elements which are present in either of the given set.
Given a set of arrays, say, ArraySet1 and ArraySet2. ﻿# Checkpoint-Introduction-to-Data-Structures-and-Procedural-programming.  

> Given a set of arrays, say, ArraySet1 and ArraySet2.  
> i, j, k: Integer variables used for iteration.  
> Sum variable is initialized to store the sum of distinct elements.  
> Processing the First Array (ArraySet1):  
> The algorithm loops through the elements of ArraySet1 using the index variable [i].  
> Furthermore, It initializes a distinct variable to TRUE to check if the current element is distinct.  
> With the aid of a nested loop, the algorithm iterates through the elements of ArraySet2 using the index variable [j]. It checks if the element at index [i] in ArraySet1 is equal to the element at index [j] in ArraySet2. If they match, the distinct is set to FALSE, indicating that it's not a distinct element.  
> If the element at index [i] in ArraySet1 is distinct, it adds it to the sum.  
> In a similar manner, the Second Array (ArraySet2) is looped for Distinct Elements: the algorithm loops through the elements of ArraySet2 using the index variable [k].  
> It also initializes a new distinct variable to TRUE.  
> Within a nested loop, it iterates through the elements of ArraySet1 using the index variable [j].  
> It checks if the element at index [k] in ArraySet2 is equal to the element at index [j] in ArraySet1. If they match, the distinct variable is set to FALSE, indicating that it's not a distinct element.  
> If the element at index [k] in ArraySet2 is distinct, it adds it to the sum.  
> Finally, the algorithm prints the value of the sum, which represents the sum of distinct elements from both arrays.  
> Practical Demonstration:   
>> Let ArraySet1 be array: [3, 1, 7, 9]  
>> Let ArraySet2 be array: [2, 4, 1, 9, 3]  
> This algorithm iterates through the ArraySet1 array and checks for each element if it is also present in the ArraySet2 array. If an element is found in both arrays, it is not added to the sum.  
>> For ArraySet1[0] (value 3), it is found in the ArraySet2 array (at index 4), so it's not added to sum.  
>> For ArraySet1[1] (value 1), it is found in the ArraySet2 array (at index 2), so it's not added to sum.  
>> For ArraySet1[2] (value 7), it is not found in the ArraySet2 array, so it's added to sum.  
>> For ArraySet1[3] (value 9), it is found in the ArraySet2 array (at index 3), so it's not added to sum.  
> In the same vein, the algorithm checks the ArraySet2 array for elements that are not in the ArraySet1 array.  
>> For ArraySet2[0] (value 2), it is not found in the ArraySet1 array, so it's added to sum.  
>> For ArraySet2[1] (value 4), it is not found in the ArraySet1 array, so it's added to sum.  
>> For ArraySet2[2] (value 1), it is found in the ArraySet1 array (at index 1), so it's not added to sum.  
>> For ArraySet2[3] (value 9), it is found in the ArraySet1 array (at index 3), so it's not added to sum.  
>> For ArraySet2[4] (value 3), it is found in the ArraySet1 array (at index 0), so it's not added to sum.  
> Sum all the elements that were added to sum in the previous steps:  
> 7 (ArraySet1[2]) + 2 (ArraySet2[0]) + 4 (ArraySet2[1]) = 13  
> So, the final value of **sum**  is 13.  

## PROBLEM 2
# Algorithm uses a proceduere called dot_product to calculates the dot(scalar) product of v1 and v2 (v1 and v2 are vectors of IR). For any n pairs of given vectors, the algorithm dtermines whether the two vectors of IR are orthogonal, by calling the procedure defined. Teh vectors are orthogonal if theie dot product equals zero.  

> # PROCEDURE PART EXPLANATION  
>> ‘PROCEDURE dot_product(v1, v2: ARRAY_OF REAL; VAR ps: REAL; n: INTEGER);'  
> This procedure calculates the dot product of two vectors v1 and v2. It takes the following parameters:  
>> v1: An array representing the first vector.  
>> v2: An array representing the second vector.  
>> ps: A variable that will store the result of the dot product.  
>> n: The dimension of the vectors, indicating how many elements are in each vector.  
> Here's a step-by-step explanation of how the dot_product procedure works:  
>> 1. Initializes the variable **ps** to 0, which will be used to accumulate the dot product.  
>> 2. The procedure enters a loop that iterates from 0 to n - 1, considering the dimension of the vectors.  
>> 3. Inside the loop, it calculates the dot product by taking the element at the same index from v1 and v2, multiplying them, and adding the result to **ps**.  
>> 4. The loop continues until it has processed all elements of the vectors.  
> Now, demonstrating the procedure with an example:  
> Suppose we have two vectors of dimension 3:  
>> Vector -> v1: [2, 3, 4]  
>> Vector -> v2: [1, 5, 2]  

> We want to calculate the dot product of these two vectors using the dot_product procedure.  
> v1 and v2 are passed as the v1 and v2 parameters to the procedure.  
>> The dimension is n = 3.  
>>Here's the calculation within the dot_product procedure:  
>> Initialize ps to 0.  
>> Loop through elements:  
>> For i = 0, we have ps = 0 + (2* 1) = 2  
>> For i = 1, we have ps = 2 + (3 * 5) = 17  
>> For i = 2, we have ps = 17 + (4 * 2) = 25  
> The final result is ps = 25, which is the dot product of the two vectors v1 and v2. In this case, the dot product is not zero, so these vectors are not orthogonal.  

> # ALGORITHM PART - DotProduct
> In addition to variables already stated above:   
>> i: an integer variable used for looping through vector pairs.  
> The algorithm starts by requesting the user to input the dimension of the vectors. The dimension is the number of elements in each vector.  
> Dimension Validation - ensured that the entered dimension is within a valid range using IF_THE_ELSE. For instance, the code checks that n is between 1 and 50. This process ensures that the dimension is within a reasonable and practical value. IF vectors dimension is valid THEN  
> The algorithm enters a loop that runs for n iterations, where n is the dimension entered by the user.  
> Inside the loop, the algorithm reads the elements of both v1 and v2 using a nested loop(s). It reads n elements for each vector. After reading the elements of v1 and v2, the algorithm calls the dot_product procedure to calculate the dot product of the two vectors (v1 and v2), passing the vectors, ’n’ and ‘ps’ variable as parameters.   
> Thereafter, the algorithm checks IF the dot product (ps) is equal to 0.  
> If ps is equal to 0, implies vectors are orthogonal, and it prints "Vectors are orthogonal."  
> If ps is not equal to 0, it implies the vectors are not orthogonal, and it prints "Vectors are not orthogonal."  
> This Algorithm is designed to process multiple pairs of vectors with the user-specified dimension and determine whether each pair is orthogonal based on the dot product.  

we define i, j, k: Integer variables used for iteration.  
Sum variable is initialized to store the sum of distinct elements.  
> Processing the First Array (ArraySet1):  
> The algorithm loops through the elements of ArraySet1 using the index variable [i].  
> Furthermore, It initializes a distinct variable to TRUE to check if the current element is distinct.  
> With the aid of a nested loop, the algorithm iterates through the elements of ArraySet2 using the index variable [j]. It checks if the element at index [i] in ArraySet1 is equal to the element at index [j] in ArraySet2. If they match, the distinct is set to FALSE, indicating that it's not a distinct element.  
> If the element at index [i] in ArraySet1 is distinct, it adds it to the sum.  
> In a similar manner, the Second Array (ArraySet2) is looped for Distinct Elements: the algorithm loops through the elements of ArraySet2 using the index variable [k].  
> It also initializes a new distinct variable to TRUE.  
> Within a nested loop, it iterates through the elements of ArraySet1 using the index variable [j].  
> It checks if the element at index [k] in ArraySet2 is equal to the element at index [j] in ArraySet1. If they match, the distinct variable is set to FALSE, indicating that it's not a distinct element.  
> If the element at index [k] in ArraySet2 is distinct, it adds it to the sum.  
> Finally, the algorithm prints the value of the sum, which represents the sum of distinct elements from both arrays.  
> Practical Demonstration:   
>> Let ArraySet1 be array: [3, 1, 7, 9]  
>> Let ArraySet2 be array: [2, 4, 1, 9, 3]  
> This algorithm iterates through the ArraySet1 array and checks for each element if it is also present in the ArraySet2 array. If an element is found in both arrays, it is not added to the sum.  
>> For ArraySet1[0] (value 3), it is found in the ArraySet2 array (at index 4), so it's not added to sum.  
>> For ArraySet1[1] (value 1), it is found in the ArraySet2 array (at index 2), so it's not added to sum.  
>> For ArraySet1[2] (value 7), it is not found in the ArraySet2 array, so it's added to sum.  
>> For ArraySet1[3] (value 9), it is found in the ArraySet2 array (at index 3), so it's not added to sum.  
> In the same vein, the algorithm checks the ArraySet2 array for elements that are not in the ArraySet1 array.  
>> For ArraySet2[0] (value 2), it is not found in the ArraySet1 array, so it's added to sum.  
>> For ArraySet2[1] (value 4), it is not found in the ArraySet1 array, so it's added to sum.  
>> For ArraySet2[2] (value 1), it is found in the ArraySet1 array (at index 1), so it's not added to sum.  
>> For ArraySet2[3] (value 9), it is found in the ArraySet1 array (at index 3), so it's not added to sum.  
>> For ArraySet2[4] (value 3), it is found in the ArraySet1 array (at index 0), so it's not added to sum.  
> Sum all the elements that were added to sum in the previous steps:  
> 7 (ArraySet1[2]) + 2 (ArraySet2[0]) + 4 (ArraySet2[1]) = 13  
> So, the final value of sum is 13.  
