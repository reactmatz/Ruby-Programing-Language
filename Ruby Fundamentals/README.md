# Ruby Roadmap - Módulo 1: Fundamentos de Ruby

## Objetivo

Este módulo tem como objetivo introduzir os conceitos fundamentais da linguagem Ruby, incluindo sintaxe básica, manipulação de strings e arrays, criação de métodos e blocks, e trabalho com arquivos.

## Conteúdo

### 1. Learn Basic Syntax

- **Data Types**: Strings, números, arrays e hashes.
    
    
    ```ruby
    string = "Hello, World!"
    number = 42
    array = [1, 2, 3, 4, 5]
    hash = {name: "Alice", age: 30}
    ```
    
- **Operators and Expressions**: Aritméticos, de comparação e lógicos.
    
    
    ```ruby
    sum = 2 + 2
    equal = 3 == 3
    not_equal = 3 != 4
    logical_and = true && false
    ```
    
- **Control Structures**: `if`, `else`, `case`, `while`, `until`, `for`.
    
    
    ```ruby
    if number > 10
      puts "Number is greater than 10"
    else
      puts "Number is 10 or less"
    end
    
    case number
    when 1
      puts "Number is 1"
    when 2
      puts "Number is 2"
    else
      puts "Number is something else"
    end
    
    while number > 0
      puts number
      number -= 1
    end
    
    for i in 0..5
      puts i
    end
    ```
    

### 2. Methods and Blocks

- **Create and Call Methods**:
    
    
    ```ruby
    def greet(name)
      "Hello, #{name}!"
    end
    
    puts greet("Alice")
    ```
    
- **Blocks,** `yield`**, and the Use of Lambdas and Procs**:
    
    
    ```ruby
    def block_example
      yield if block_given?
    end
    
    block_example { puts "Hello from a block!" }
    
    lambda_example = ->(x) { x * 2 }
    puts lambda_example.call(10)
    
    proc_example = Proc.new { |x| x * 2 }
    puts proc_example.call(10)
    ```
    

### 3. String and Array Manipulation

- **Useful Methods like** `.map`**,** `.select`**,** `.reduce`**,** `.each`:
    
    
    ```ruby
    numbers = [1, 2, 3, 4, 5]
    
    doubled = numbers.map { |n| n * 2 }
    evens = numbers.select { |n| n.even? }
    sum = numbers.reduce(0) { |acc, n| acc + n }
    
    numbers.each { |n| puts n }
    ```
    

### 4. Working with Files

- **Read, Write, and Manipulate Files with Ruby (**`File`**,** `IO`**)**:
    
    ````ruby
  File.open("example.txt", "w") do |file|
  file.puts "Hello, file!"
end
File.open("example.txt", "r") do |file|
  puts file.read
end````