# interviewbit--maths--rearrange array


**-----> Question:**

Rearrange a given array so that Arr[i] becomes Arr[Arr[i]] with O(1) extra space.

Example:

Input : [1, 0]
Return : [0, 1]
Lets say N = size of the array. Then, following holds true :

All elements in the array are in the range [0, N-1]
N * N does not overflow for a signed integer


**-----> Code:**

void Solution::arrange(vector<int> &A) {
  
    // Do not write main() function.
    // Do not read input, instead use the arguments to the function.
    // Do not print the output, instead return values as specified
    // Still have a doubt. Checkout www.interviewbit.com/pages/sample_codes/ for more details

    int n=A.size();

    for(int i=0;i<n;i++){
        A[i]=A[i]+ (A[A[i]]%n)*n;
    }

    for(int i=0;i<n;i++){
        A[i]=A[i]/n;
    }

    return;
}
