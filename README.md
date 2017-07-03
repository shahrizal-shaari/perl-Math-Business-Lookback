# NAME

Math::Business::LookBacks

# SYNOPSIS

    use Math::Business::LookBacks;

    # price of a Lookback Fixed Call option

    my $price_lbfixedcall_option = Math::Business::LookBacks::lbfixedcall(
        1.35,       # stock price
        1.36,       # barrier
        (7/365),    # time
        0.002,      # payout currency interest rate (0.05 = 5%)
        0.001,      # quanto drift adjustment (0.05 = 5%)
        0.11,       # volatility (0.3 = 30%)
        1.39,       # maximum spot
        undef       # minimum spot
    );

# DESCRIPTION

Prices lookbacks options using the GBM model, all closed formulas.

# SUBROUTINES

## lbfloatcall

    USAGE
    my $price = lbfloatcall($S, $K, $t, $r_q, $mu, $sigma, $S_max, $S_min)

    DESCRIPTION
    Price of a Lookback Float Call

## lbfloatput

    USAGE
    my $price = lbfloatcall($S, $K, $t, $r_q, $mu, $sigma, $S_max, $S_min)

    DESCRIPTION
    Price of a Lookback Float Put

## lbfixedcall

    USAGE
    my $price = lbfixedcall($S, $K, $t, $r_q, $mu, $sigma, $S_max, $S_min)

    DESCRIPTION
    Price of a Lookback Fixed Call

## lbfixedput

    USAGE
    my $price = lbfixedput($S, $K, $t, $r_q, $mu, $sigma, $S_max, $S_min)

    DESCRIPTION
    Price of a Lookback Fixed Put

## lbhighlow

    USAGE
    my $price = lbhighlow($S, $K, $t, $r_q, $mu, $sigma, $S_max, $S_min)

    DESCRIPTION
    Price of a Lookback High Low

## d1\_function

returns the d1 term common to many BlackScholes formulae.

## dnorm

Standard normal density function

## l\_max

This is a common function use to calculate the lookbacks options price. See \[1\] for details.

## l\_min

This is a common function use to calculate the lookbacks options price. See \[1\] for details.

# DEPENDENCIES

    * Math::CDF

# SOURCE CODE

    https://github.com/binary-com/perl-Math-Business-LookBacks

# REFERENCES

\[1\] Espen Gaarder Haug, PhD
    The Complete Guide to Option Pricing Formulas p141-p144

# AUTHOR

binary.com, `<shahrizal at binary.com>`

# BUGS

Please report any bugs or feature requests to

`bug-math-business-lookbacks at rt.cpan.org`, or through the web

interface at

[http://rt.cpan.org/NoAuth/ReportBug.html?Queue=Math-Business-LookBacks](http://rt.cpan.org/NoAuth/ReportBug.html?Queue=Math-Business-LookBacks).

I will be notified, and then you'll automatically be notified of progress on

your bug as I make changes.

# SUPPORT

You can find documentation for this module with the perldoc command.

    perldoc Math::Business::LookBacks

You can also look for information at:

- RT: CPAN's request tracker (report bugs here)

[http://rt.cpan.org/NoAuth/Bugs.html?Dist=Math-Business-LookBacks](http://rt.cpan.org/NoAuth/Bugs.html?Dist=Math-Business-LookBacks)

- AnnoCPAN: Annotated CPAN documentation

[http://annocpan.org/dist/Math-Business-LookBacks](http://annocpan.org/dist/Math-Business-LookBacks)

- CPAN Ratings

[http://cpanratings.perl.org/d/Math-Business-LookBacks](http://cpanratings.perl.org/d/Math-Business-LookBacks)

- Search CPAN

[http://search.cpan.org/dist/Math-Business-LookBacks/](http://search.cpan.org/dist/Math-Business-LookBacks/)
