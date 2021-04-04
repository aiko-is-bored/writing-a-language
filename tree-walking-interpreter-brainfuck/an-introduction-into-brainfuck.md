# An introduction into Brainfuck

{% hint style="warning" %}
Warning: This page and section will use vulgar language like a sailor. If you value your sanity, please read the article as if the "fuck" did not exist.
{% endhint %}

{% tabs %}
{% tab title="Wikipedia" %}
Brainfuck is an esoteric programming language created in 1993 by Urban Müller. Notable for its extreme minimalism, the language consists of only eight simple commands and an instruction pointer. While it is fully Turing complete, it is not intended for practical use, but to challenge and amuse programmers.
{% endtab %}

{% tab title="Uwu-fied" %}
Bwainfuck is an esotewic pwogwamming wanguage cweated in 1993 by U-U-Uwban Müwwew. Nyotabwe fow its extweme minyimawism, the x3 wanguage consists of onwy eight simpwe commands :3 and an instwuction pointew. Whiwe i-it is fuwwy Tuwing ;;w;; compwete, i-it is nyot intended owo fow pwacticaw use, but t-to chawwenge and a-amuse p-p-pwogwammews.
{% endtab %}
{% endtabs %}

Brainfuck is an extremely minimal language that serves as a great introduction into writing a programming language. It consists of only 8 symbols, a pointer, and a virtual tape:

| Symbols | Meaning |
| :--- | :--- |
| &gt; | Increment the pointer |
| &lt; | Decrement the pointer |
| + | Increment the pointed cell |
| - | Decrement the pointed cell |
| , | Pull one character out of the `stdin` |
| . | Push one character to the `stdout` |
| \[ | Start of a loop, repeat content inside brackets |
| \] | End of a loop, go back to the start if the current cell is not at value zero |

Now you may be confused, asking what the tape is, what a cell is, or what the tape is. Here's a quick explanation:

```text
[0,6,12,18]
 ^
 |
 
 Pointer: 0
 Cell_value: 0 
 [0,6,12,18]
    ^
    |

Pointer: 1
Cell_value: 6

[0,6,12,18]
     ^
     |
     
Pointer: 2
Cell_value: 12

Let's run a command:

>+

Tape:

[0,6,12,19]
        ^
        |
Pointer: 3,
Cell_value: 19
```

Basically, the tape is just an array or slice of values, and the pointer is the number of the element, the cell is the element we are pointing to. Got it? Good.



Let's look at `stdio` now. 

The `,` gets one character out of the STDIN and inserts the ASCII value of that character into the pointed cell. The `.` does the opposite, it prints out the character version of the ASCII value inside the cell.

```text
[72,125,0]
 ^
 |
 
 Run command:
 
 .>.

 Output:

 "Hi"
 
 Result:
 
 [72,125,0]
      ^
      |
 
 
 [0]
 
 Run command:
 
 ,
 
 Input:
 
 H
 
 Result:
 [72]
 
```

Now that you know how to write code in Brainfuck, try writing "Hello world!" \(you can use a text to ASCII converter, don't worry\).

{% tabs %}
{% tab title="Task" %}
Try writing a Brainfuck program that outputs `Hello world` to the terminal. You can use [Brainfuck Interpreter](https://copy.sh/brainfuck/) to test your code. Stuck? Check the solution.
{% endtab %}

{% tab title="Solution" %}
```text
+[-[<<[+[--->]-[<<<]]]>>>-]>-.---.>..>.<<<<-.<+.>>>>>.>.<<.<-.
```
{% endtab %}
{% endtabs %}

Don't worry if you didn't solve it, it's perfectly fine. Anyhow, let's continue on and cover some basic Brainfuck algorithms and then we'll write an interpreter for the language.

