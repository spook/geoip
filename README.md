# geoip
Simple GeoIP Address Lookup Tool

Dumps the geolocation information for an IP address.
Compact and verbose outputs are available.
This is just a wrapper around the Perl Geo::IP module
(for v1 format databases), or the Perl GeoIP2::Database::Reader 
module (for v2 format databases).

## SYNOPSIS

    $ geoip 1.1.1.1
    OC|AU|Australia|07|Victoria||Research|Australia/Melbourne|-37.7000|145.1833

    $ geoip -v 1.1.1.1
      Country Code: AU
      Country Name: Australia
            Region: 07
       Region Name: Victoria
        Metro Code: --
              City: Research
         Time Zone: Australia/Melbourne
          Location: (-37.7000,145.1833)
    GeoIP Database: /usr/share/GeoIP/GeoIPCity.dat

The summary (non-verbose) fields are in the same order as the verbose output.
Fields without values are shown with a double-dash (--).

## INSTALLATION

Simply copy the `geoip` script to someplace in your $PATH.
Make sure it's executable.

Then, you'll need a copy of MaxMind's GeoIP database.
There's various databases of varying precision; some are free and some cost.
See https://dev.maxmind.com/geoip/legacy/downloadable/ for databases.

Obtain a suitable database and place it on your system;
I suggest `/usr/local/share/GeoIP/`.  Then edit the `geoip` script to make 
it open that particular database file (see line 7).

That's it... enjoy!
