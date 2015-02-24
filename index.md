% Welcome to Rust!

Andrew Clarkson

February 24th, 2015

# Big Thanks!

- Code 42
- Sam

# Quick Poll

Raise your hands don't be shy...

# What the Heck is Rust?
A systems programming language designed to be:

- fast
- concurrent
- safe

# Origin Story

Why create _another_ language?

# Where Are We At?

- alpha2 (feature complete)
- under heavy development
- nightlies

# Milestones

- alpha2 released on Friday (February 20th, 2015)
- stable planned for March 9th, 2015
- beta planned for March 31st, 2015
- 1.0 planned for May 15th, 2015

# Rust Wants You!

- alpha2: Grok API's
- stable: Refactor crates
- beta: Test and polish!

# Why is Rust so Cool

Based on some fine Rustaceans on Reddit:

- Memory model
- Algebraic Data Types
- Functional Style
- Scoping, Modules, &amp; Crates 
- No Cost Abstraction
- The Community

# Memory

- Efficient
- Safe

# Borrowing & Regions
```rust
fn borrow(x: &int) {
    println!("{:?}", x);
}

let x = 10;
borrow(&x);
```
# Owned Stuff
```rust
fn own(x: Box<int>) {
    // x dies here
}
{
    let x = Box::new(7);
    own(x);
}
```

# Algebraic Data Types
```rust
enum Option<T> {
    Some(T),
    None
}
```
# Functional Style
```
use std::iter;
use std::iter::AdditiveIterator;

let sum: u32 =
    iter::count(0, 1).
    map(|n| n * n).
    take_while(|&n| n < 1000u32).
    filter(|n| is_odd(*n)).
    sum();

fn is_odd(n: u32) -> bool { n % 2 == 1 }
```
# Modules and Crates
- No more `ngx_printf`
- Real package manager
# No Cost Abstraction
```
trait Barking {
    fn bark(&self);
}

fn make_bark<T: Barking>(barker: T) {
    barker.bark();
}
```

# What is it good for?
- Game Development
- Servo
- Data Science
- Databases
- Servers
- Embedded
- ?



