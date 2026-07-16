# Remove-Duplicates-from-Sorted-Array-II
nums=list(map(int,input("Enter sorted array elements:").split()))
n=len(nums)
if n<=2:
    print("Length:",n)
    print("Array:",nums)
else:
    c=2
    for i in range(2,n):
        if nums[i]!=nums[c-2]:
            nums[c]=nums[i]
            c+=1
    print("Length:",c)
    print("Array after removing extra duplicates:",nums[:c])
