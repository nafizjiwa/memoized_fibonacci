# Memoized_fibonacci

Create a memoized fibonacci() function. This function should return the nth Fibonacci number.

Note: To avoid an infinite loop, <br />
either handle the edge case of negative numbers in your function, <br />
or don’t call it using negative numbers.

      memo = {}
      
      def fibonacci(num):
        answer = None
        # Write your code here
        if num in memo:
          answer = memo[num]
        elif num == 0 or num == 1:
          answer = num
        else:
          answer = fibonacci(num - 1) + fibonacci(num - 2)
          memo[num] = answer
        return answer

# Test your code with calls here:
`print(fibonacci(20))` <br />
`print(fibonacci(200))`
