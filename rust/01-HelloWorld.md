# 1: Hello World - Rust

In this lesson, we will learn how to install cargo (the Rust package manager), create a project, and write a "Hello World" program in the Rust programming language.

## Installing Rust

In order to install Rust, install the `rustup` package.

This can be done using your default package manager (on Linux) or using the following command:

``` sh
curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh
```

If you are using Windows, please use [this document](https://doc.rust-lang.org/book/ch01-01-installation.html) by the official Rust foundation to help you install Rustup.

The `rustup` package should now contain a copy of cargo - to verify, type the following command:

``` sh
cargo --version
```

Expected output (version number will be different):

``` output
cargo 1.72.0 (103a7ff2e 2023-08-15)
```

## Creating a project

In order to create a project using cargo, type the following command:

``` sh
cargo new hellorust && cd hellorust
```

This creates the `hellorust` project and opens the project in a terminal.

Now simply open the `hellorust` folder in a code editor. For example...

``` sh
codium .
```

... will open the current folder in VS Codium

## Coding

Inside the `src` folder, you will see the `main.rs` file.

This file contains the main source code for our program.

Inside, you will see the following code:

``` rs
fn main()
{
  println!("Hello, world!");
}
```

This program prints the text `Hello, world!` to the screen. We will explain the code more in a minute.

First, let's focus on running our program.

## Running our program

To run our program, simply type the following into a terminal:

``` sh
cargo run
```

> Not working? Make sure you are in the `hellorust` folder. Use the `cd` command to get there!

This should give the following output:

``` text
   Compiling hellorust v0.1.0 (/home/dylan/coding/hellorust)
    Finished dev [unoptimized + debuginfo] target(s) in 0.29s
     Running `target/debug/hellorust`
Hello, world!
```

Note: Throughout this course, we will not display the compiler messages in the program output.

Therefore, the output of the above program will simply be displayed as:

``` text
Hello, world!
```

Congratulations! You have written your first Rust program.

But how does it work?

## How it works

This is our `Hello World` program:

``` rs
1 fn main()
2 {
3   println!("Hello, world!");
4 }
```

### Line 1

``` rs
fn main()
```

We declare the `main` function.  
The `main` function is executed (run) when we run our program.  
To create a function, we type `fn name(params)`, where:

* `name` is the name of the function
* `params` is a list of parameters (these are given to the function when we call it)

### Line 2 and 4

``` rs
{
	...
}
```

Here, we are declaring the function body.  
Everything inside the curly brackets is part of the function.

### Line 3

``` rs
println!("Hello, world!");
```

The `println!` identifier is a **macro**.  
Essentially, it works like a function - we can call it and pass it arguments.

In our case, we are calling `println!` with the argument `"Hello, world!"`.  
This is called a `string`, and it is essentially just some text.

We end the statement with a semicolon.  
We need to do this so that Rust knows we are finished printing things to the screen.

## Reference

`function` - Can be called and given arguments  
`macro` - Similar to a function, can be called and recieve parameters  
`println!` - A macro which prints text to the screen  
`string` - A data type that contains text  
`Cargo` - A tool for managing Rust projects  
`main` - The function that is called when a program starts up  
`compiler` - A program which converts human code (e.g. .rs files) into machine code (binary)    

## Links

[Back to contents](README.md)  
[Next lesson (Variables)](02-Variables.md)  
