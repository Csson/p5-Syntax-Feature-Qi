# NAME

Syntax::Feature::Qi - Remove the same indendation from all lines in a string

<div>
    <p>
    <img src="https://img.shields.io/badge/perl-5.10+-blue.svg" alt="Requires Perl 5.10+" />
    <a href="https://travis-ci.org/Csson/p5-Syntax-Feature-Qi"><img src="https://api.travis-ci.org/Csson/p5-Syntax-Feature-Qi.svg?branch=master" alt="Travis status" /></a>
    <a href="http://cpants.cpanauthors.org/dist/Syntax-Feature-Qi-1.0000"><img src="https://badgedepot.code301.com/badge/kwalitee/Syntax-Feature-Qi/1.0000" alt="Distribution kwalitee" /></a>
    <a href="http://matrix.cpantesters.org/?dist=Syntax-Feature-Qi%201.0000"><img src="https://badgedepot.code301.com/badge/cpantesters/Syntax-Feature-Qi/1.0000" alt="CPAN Testers result" /></a>
    <img src="https://img.shields.io/badge/coverage-97.4%-yellow.svg" alt="coverage 97.4%" />
    </p>
</div>

# VERSION

Version 1.0000, released 2016-04-16.

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

This software is copyright (c) 2016 by Erik Carlsson.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.
