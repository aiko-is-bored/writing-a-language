---
description: An introduction into the series.
---

# Introduction

## Introduction

Hello and welcome to this GitBook! In this series, we'll write many different types of compilers and interpreters. This series is designed in such a way that each section builds on the other section. This section will give a basic overview over the sections. The book assumes you know one of the following languages:  


* JavaScript or TypeScript
* Rust
* C++
* C
* Go/Golang

This book is primarily intended towards Rust & TypeScript audiences, but offers detailed and explained examples in the other languages.

{% hint style="info" %}
As the writer of this book, I just wanted to inform you that I primarily write my code in TypeScript, Rust, Go, and Water \(a programming language I wrote, just to flex\). If you are of native CPP or C tongue, please feel free to contribute to the GitBook.
{% endhint %}

### Overview

In this book, we will cover four different types of languages:

* VM-less compilers
* Tree-walking interpreters
* VM compilers
* Virtual Machines \(yes they count too!\)
* JIT interpreters

#### VM-less compiled languages

In this section, we'll go over languages that compile to another representation or compile directly to machine code. Since **LLVM IR** isn't actually a VM IR, we'll include it in this section. We'll cover different methods of writing a **transpiler** or **native compiler**.

#### Tree-walking interpreters

In this section, we'll go over what a tree-walking interpreter is and we'll write a small tree-walking interpreter for a subset of JavaScript.

#### Virtual Machines

Here, we'll touch on what a virtual machine is, the different types of virtual machines, as well as a few implementations of virtual machines \(ex. The JVM\). We'll also write our own small stack-based VM.

#### VM compilers

For the final type, we'll go over how languages are actually compiled to virtual machines, and write a compiler that compiles to the JVM bytecode.

#### JIT interpreters

In this section, we'll discuss what a JIT interpreter is, why people write them, and write a small JIT interpreter for a subset of JavaScript.

As you can see, we'll be covering a lot in this book. But that's not all, as we'll get into implementations very quickly. Here's the complete roadmap:



* Writing an interpreter 

