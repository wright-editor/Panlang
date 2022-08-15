# Panlang: a programming language converter
Inspired by pandoc and guile, this tool will convert various programming languages to an abstract syntax tree that can then be converted to any other compatible languages. 

## Reasoning
I want to create this tool as a way to create intercompatible configurations languages. This way, programs could be extended using any language preferred by the user. Particularly, I want to use this tool as the configuration framework for the wright-editor.

## Limitations
Most existing languages will be incompatible with this idea. Instead, this tool should be used as a language creation framework. Languages created within this framework will not be as flexible as normal languages, they will instead conform to a specification defined in rust. Any structures not created in every language will be copied entirely instead of referenced when converted. 

# Implementation
This tool will be implemented in Rust. I am choosing this language because it is relatively easy to make programs memory safe. Languages should be able to import the abstract sytax tree of Panlang as ifthey were the same language.

## everything is a peg grammar
All languages created using this tool as a framework will be specified using a PEG grammar in rust, using the peg-rust crate. This standardizes language creation.

Another alternative would be a context free grammar, but this might limit the possible languages.

## First language
The first language that will be created and will be used as a testing language for Panlang is a variant of lisp. Eventually I hope to implement a form of lua as well as a form of EMCAscript. 
