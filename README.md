# NAME

Net::DNS::Resolver::Mock - Mock a DNS Resolver object for testing

# DESCRIPTION

A subclass of Net::DNS::Resolver which parses a zonefile for it's data source. Primarily for use in testing.

[![Code on GitHub](https://img.shields.io/badge/github-repo-blue.svg)](https://github.com/marcbradshaw/Net-DNS-Resolver-Mock)

[![Build Status](https://travis-ci.org/marcbradshaw/Net-DNS-Resolver-Mock.svg?branch=master)](https://travis-ci.org/marcbradshaw/Net-DNS-Resolver-Mock)

[![Open Issues](https://img.shields.io/github/issues/marcbradshaw/Net-DNS-Resolver-Mock.svg)](https://github.com/marcbradshaw/Net-DNS-Resolver-Mock/issues)

[![Dist on CPAN](https://img.shields.io/cpan/v/Net-DNS-Resolver-Mock.svg)](https://metacpan.org/release/Net-DNS-Resolver-Mock)

[![CPANTS](https://img.shields.io/badge/cpants-kwalitee-blue.svg)](http://cpants.cpanauthors.org/dist/Net-DNS-Resolver-Mock)

# SYNOPSIS

    use Net::DNS::Resolver::Mock;

    my $Resolver = Net::DNS::Resolver::Mock-new();

    $Resolver->zonefile_read( $FileName );
    # or
    $Resolver->zonefile_parse( $String );

# PUBLIC METHODS

- zonefile\_read ( $FileName )

    Reads specified file for zone data

- zonefile\_parse ( $String )

    Reads the zone data from the supplied string

- die\_on ( $Name, $Type, $Error )

    Die with $Error for a query of $Name and $Type

- set\_debug ()

    Once set, the resolver will write any lookups received to STDERR

# DEPENDENCIES

    Net::DNS::Resolver
    Net::DNS::Packet
    Net::DNS::Question
    Net::DNS::ZoneFile

# BUGS

Please report bugs via the github tracker.

https://github.com/marcbradshaw/Net-DNS-Resolver-Mock/issues

# AUTHORS

Marc Bradshaw, <marc@marcbradshaw.net>

# COPYRIGHT

Copyright (c) 2017, Marc Bradshaw.

# LICENCE

This library is free software; you may redistribute it and/or modify it
under the same terms as Perl itself.
