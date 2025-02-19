# Rust Undefined Behavior Example

This repository demonstrates a common source of undefined behavior in Rust: modifying a vector through a raw pointer after the vector's capacity might have changed.  The code attempts to modify the first element of a vector using a raw pointer. This is dangerous because if the vector needs to reallocate (e.g., if you add more elements), the pointer becomes invalid and leads to unpredictable results. 

The solution shows how to avoid this by using safe Rust methods to manipulate vector elements.