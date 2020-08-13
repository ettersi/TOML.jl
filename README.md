# TOML.jl

A [TOML v1.0.0](https://github.com/toml-lang/toml) parser for Julia.

[![Build Status](https://travis-ci.org/wildart/TOML.jl.svg?branch=master)](https://travis-ci.org/wildart/TOML.jl)
[![Coverage Status](https://coveralls.io/repos/wildart/TOML.jl/badge.svg?branch=master&service=github)](https://coveralls.io/github/wildart/TOML.jl?branch=master)
[![Build status](https://ci.appveyor.com/api/projects/status/quhhe2m3e9vbim6u?svg=true)](https://ci.appveyor.com/project/wildart/toml-jl)

*Note:*  This is a Julia standard library and does not need to be explicitly
installed.

## Basic Usage

```julia

julia> import TOML

julia> TOML.parse("""
       name = "value"
       """)
Dict{AbstractString,Any} with 1 entry:
  "name" => "value"

julia> TOML.parsefile("etc/example.toml")
```

## Documentation
```julia
TOML.print(io::IO, a::AbstractDict)
```
Writes a TOML representation to the supplied `IO`.

```julia
TOML.parse(s::AbstractString)
TOML.parse(io::IO)
TOML.parsefile(filename::AbstractString)
```
Parses a TOML `AbstractString` or `IO` stream into a nested `Array` or `Dict`.
