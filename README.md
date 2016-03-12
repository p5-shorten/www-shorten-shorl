# NAME

WWW::Shorten::Shorl - Perl interface to [http://shorl.com](http://shorl.com)

# SYNOPSIS

```perl
use strict;
use warnings;

use WWW::Shorten 'Shorl'; # recommended
# use WWW::Shorten::Shorl; # also available

my $long_url = 'http://www.foo.com/bar/';
my $short_url = makeashorterlink($long_url);
my ($short_url,$password) = makeashorterlink($long_url);

$long_url = makealongerlink($short_url);
```

# DESCRIPTION

**WARNING:** [http://shorl.com](http://shorl.com) does not provide an API.  We must scrape the
resulting HTML.

- Also, they prevent multiple usages of their service within a changing time
frame.  Due to this, all live tests against this service have been skipped.
- You have been warned.  We suggest using another [WWW::Shorten](https://metacpan.org/pod/WWW::Shorten) service.

A Perl interface to the web site [http://shorl.com](http://shorl.com).  That service simply maintains
a database of long URLs, each of which has a unique identifier.

# Functions

[WWW::Shorten::Shorl](https://metacpan.org/pod/WWW::Shorten::Shorl) makes the following functions available.

## makeashorterlink

The function ```makeashorterlink``` will call use the web service, passing it
your long URL and will return the shorter version. If used in a
list context, then it will return both the shorter URL and the password.

Note that this service, unlike others, returns a unique code for every submission.

## makealongerlink

The function ```makealongerlink``` does the reverse. ```makealongerlink```
will accept as an argument either the full short URL or just the
service's identifier.

If anything goes wrong, then either function will return ```undef```.

# AUTHOR

Iain Truskett spoon@cpan.org

# CONTRIBUTORS

- Chase Whitener capoeirab@cpan.org -- current maintainer
- Dave Cross dave@perlhacks.com

=back

# COPYRIGHT AND LICENSE

See the main [WWW::Shorten](https://metacpan.org/pod/WWW::Shorten) docs.