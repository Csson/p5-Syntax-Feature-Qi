# NAME

Syntax::Feature::Qi - Remove the same indendation from all lines in a string

# VERSION

Version 0.2003, released 2015-01-17.

# SYNOPSIS

    use syntax 'qi';

    say qi{
        This is a sub routine:
        sub printme {
            print shift;
        }
    };

    # is exactly the same as

    say qi{
    This is a sub routine:
    sub printme {
        print shift;
    }
    };

# DESCRIPTION

This is a syntax extension to be used with [syntax](https://metacpan.org/pod/syntax).

It provides two quote-like operators, `qi` and `qqi`. They are drop-in replacements for `q` and `qq`, respectively.

They work like this: First they find the first line in the string with a non-white space character. It saves the
white space from the beginning of that line up to that character, and then it tries to remove the exact same whitespace from
all other lines in the string.

# SEE ALSO

- [Syntax::Feature::Ql](https://metacpan.org/pod/Syntax::Feature::Ql) (which served as a base for this)
- [Syntax::Feature::Qs](https://metacpan.org/pod/Syntax::Feature::Qs)
- [String::Nudge](https://metacpan.org/pod/String::Nudge)
- [syntax](https://metacpan.org/pod/syntax)

# SOURCE

[https://github.com/Csson/p5-Syntax-Feature-Qi](https://github.com/Csson/p5-Syntax-Feature-Qi)

# HOMEPAGE

[https://metacpan.org/release/Syntax-Feature-Qi](https://metacpan.org/release/Syntax-Feature-Qi)

# AUTHOR

Erik Carlsson <info@code301.com>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2015 by Erik Carlsson.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.
