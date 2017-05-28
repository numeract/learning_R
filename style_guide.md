# Code Style Guide

## R Style Guide

Main guide: [tidyverse style guide](http://style.tidyverse.org/)

Below are more specific guidelines


## Comments and documentation

- Always in English, run spell-checker
- Explain *Why* not *What* (assume people know the programming language)
    + leave a space after the comment symbol, as in `# `

## Naming

- **Watch [The Naming of Ducks](https://www.youtube.com/watch?v=YklKUuDpX5c)**
- Where the language and the previous code base allow, variable names should follow the pattern `my_variable` (no CamelCase, just use underscore)
    + This works for Python, R and SQL identifiers
- Functions names should be verbs
    + except for math-line functions such as `cos()`
    + should fit on one page (if longer, think about creating a second function)
- If using [Hungarian notation](https://en.wikipedia.org/wiki/Hungarian_notation), consider using the suffixes from `purrr::`, such as `_dbl`, `_lgl`, etc.
    + other suffixes: 
        + `_msk`: mask for logical/selecting within a vector
        + `_idx`: index, as in `var_idx <- which(var_msk)`
- Table / collection / list names: singular or plural?
    + [good subjective discussion](http://stackoverflow.com/questions/338156/table-naming-dilemma-singular-vs-plural-names)
    + *preference for singular*
    + use singular for dataframes, SQL tables, ORM classes
    + use plural for vectors, e.g.,  `customer_names`
    + *consistency is key*