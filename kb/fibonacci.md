# 1. The function approach - skip if not using a function

## Define the function

```py
def fibonacci():
```

## Add function inputs

```py
def fibonacci(fibonacci_sequence, number):
```

# 2. Define the inputs

## Using the function approach

```py
fibonacci([1,1], 10) # 10 can be any number
```

## No function

```py
fibonacci_sequence = [1,1]
number = 10
```

# 3. Open the loop

```py
for current_num in range(start, end):
```

What should `start` and `end` be? What do we know?
- how many fibonacci numbers do we already have in our sequence list?
    - do list indexes start at 0 or 1? so what should `start` be?

- we want a list of all the fibonacci numbers up to `number`, so what should end be?

# 4. Figuring out the algorithm

What do we know?

We know that the sequence is the result of adding together the 2 previous fibonacci numbers.

So if the current number is 10, then we want to add fibonacci(9) and fibonacci(8).. or.. fibonacci(10-1) + fibonacci(10-2)

- so, what is the fibonacci of `current_num`?
- Do we have the 2 previous fibonacci numbers stored anywhere?
- How do we access them from a list?

<details>
<summary>Spoiler Alert!</summary>

```py
next_number = fibonacci_sequence[current_num-1] + fibonacci_sequence[current_num-2]
```

</details>

- How do we add the new result to the list?

<details>
<summary>Spoiler Alert!</summary>

```py
fibonacci_sequence.append(next_number)
# or
fibonacci_sequence += [next_number]
# or
fibonacci_sequence[current_num] = next_number
```

</details>

Print `fibonacci_sequence` at the end of the function or file to check that it worked.

# Problem part B

Sum the total of all numbers in the list without using `sum()`.

What do we know?

- We need to track a total.
- We have the `next_number` variable in our loop that currently stores the current number.

Questions:

1. How can we store the total and should we define it inside or outside the loop?
2. How can we add each new result to the total? Should we do that inside or outside the loop?
