## find right most bit
n & -n(2s complement)
n & (~n+1)

# if n is 2^
n && !(n & n-1)
