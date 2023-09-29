n = int(input())
a = list(map(int, input().split()))
b = list(map(int, input().split()))

index_one = None
index_two = None

for i in range(n):
    if a[i] != b[i]:
        index_one = i
        break

for i in range(n - 1, -1, -1):
    if a[i] != b[i]:
        index_two = i
        break

if index_one is None:
    print("YES")
else:
    if all(a[i] <= b[i] for i in range(index_one, index_two + 1)):
        a[index_one:index_two + 1] = sorted(a[index_one:index_two + 1])

        if a == sorted(a):
            print("YES")
        else:
            print("NO")
    else:
        print("NO")

<!---
Lamentis/Lamentis is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
