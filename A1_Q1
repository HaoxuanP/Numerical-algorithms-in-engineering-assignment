# Read input file
with open('q1_in.txt','r') as q1_in:
    n = int(q1_in.readline()) # total len of list
    vis_list = list(map(float, q1_in.readline().split())) # convert to list of float
    k = int(q1_in.readline()) # sum of a+b


# Initialise starting combination 
a = k
b = 0

cur_sum = sum(vis_list[:k]) #sum of first k numbers
max_sum = cur_sum

# Loop through all possible combinations of a & b and their sum
for i in range(1,k+1):

    # update values of a & b
    cur_a = k-i
    cur_b = i

    # keep the current sum and add+substract elements from the sum
    cur_sum -= vis_list[k-i] 
    cur_sum += vis_list[n-i]

    # find best combination of a & b for max sum
    if cur_sum > max_sum:
        max_sum = cur_sum
        a = cur_a
        b = cur_b

# Write answers as output file
with open('q1_out.txt','w') as q1_out:
    q1_out.write(str(a) + '\n')
    q1_out.write(str(b))



# Note: possible for more than 1 combination for a+b to give max
