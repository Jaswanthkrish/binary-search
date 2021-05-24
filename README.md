# binary-search
def search(list, n):

    l = 0
    h = len(list)-1

    while l <= h:
        mid = (l+h) // 2

        if list[mid] == n:
            
            return True
    
        else:
            if list[mid] < n:
                l = mid+1
            else:
                h = mid-1

    return False



list = [4,7,8,12,45,99,102,702,10987,56666]
n = 10
list.sort()
print(list)


if search(list, n):
    x=list.index(n)
    print("Found at ",x)
else:
    print("Not Found")
