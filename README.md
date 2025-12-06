# Discrete-Math

# Score values within code

def Insert_Sort(a):
    shifts = 0
    a = a[:]

    for i in range(1,len(a)):
        x = a[i]
        j = i - 1
        moved = False
        
        while j >= 0 and x > a[j]:
            a[j+1] = a[j]
            shifts +=1
            moved = True
            j -=1

        a[j+1] = x
        
        if moved:
            shifts += 1

    return a, shifts
scores = [100, 85, 95, 70]
sort, shifts = Insert_Sort(scores)
print(f"Sorted List: {sort} .Total Shifts: {shifts}")

###################################################################
# Code using User Inputs

def Insert_Sort(a):
    shifts = 0
    a = a[:]

    for i in range(1,len(a)):
        x = a[i]
        j = i - 1
        moved = False
        
        while j >= 0 and x > a[j]:
            a[j+1] = a[j]
            shifts +=1
            moved = True
            j -=1

        a[j+1] = x
        
        if moved:
            shifts += 1

    return a, shifts

scorelist = input(f"Enter the scores(Example: 10 20 30 40 50): ")
scores = list(map(int, scorelist.split()))

sorted_scores, total_shifts = Insert_Sort(scores)

print(f"Sorted List: {sorted_scores}. Total Shifts: {total_shifts}")
