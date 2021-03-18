# Type System
My notes on type systems in different languages. 

## C Language

```
                                             Types
                                             
[const] [volatile] T                                     Sized type (types always have size)
([const] [volatile] T) * [const] [volatile]              Pointer type (points to some another type)
[const] [volatile] int|double|float|char|...             Arithmetic type (can be converted to each other)

in case of copying
[c][v] T -> [c][v] T                                     Any type without qualifier can be converted to the 
                                                         type with qualifier

T       - just type with some qualifiers
aT      - arithmetic type
pT      - pointer type

                                             Type casting

(aA|pA) aB|pB                                            Will convert type on right to type on left
                                                         (in paranthethis)
                                                         only works with arithmetic and pointer
                                                         types

If you want to convert your custom type to other custom type, only way to do that is 
with pointer types (it will perform copying):

A convert(B) { return *((A*)B*); }
will transform B -> A           

                                             Special type
                                             
void                                                     Type that doesn't have size and means nothing
void* [const] [volatile]                                 Just pointer (Pointer type) to anything
                                                         (size of value that it's points to is undefined)
                                                         
Useful in case of malloc(). When we're allocating memory and we don't know value of which type
user will put in this memory location. So we return void* that will be converted by user
to any type he wants (of course, he can fuck up with size of value, but it's his problem).
```

## Rust


## Java
