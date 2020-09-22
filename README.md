# geoip
Simple GeoIP Address Lookup Tool

Dumps the geolocation information for an IP address.
Compact and verbose outputs are available.
This is just a wrapper around the Perl Geo::IP module;
there's nothing fancy or magical here.
I've written this so many times over and over, 
I finally made it "real".  

Here it is, I hope it saves you a few hundred keystrokes!

## SYNOPSIS

    $ geoip 1.1.1.1
    OC|AU|AUS|Australia|07|Victoria||Research|3095|Australia/Melbourne||-37.7000|145.1833

    $ geopi -v 1.1.1.1
      Country Code: AU
    Country Code 3: AUS
      Country Name: Australia
            Region: 07
       Region Name: Victoria
        Metro Code: --
              City: Research
       Postal Code: 3095
         Time Zone: Australia/Melbourne
         Area Code: --
          Location: (-37.7000,145.1833)

The summary (non-verbose) fields are in the same order as the verbose output.
Fields without values are shown with a double-dash (--).

## INSTALLATION

Simply copy the `geoip` script to someplace in your $PATH.
Make sure it's executable.

Then, you'll need a copy of MaxMind's GeoIP database.
There's various databases of varying precision,;some are free and some cost.
See https://dev.maxmind.com/geoip/legacy/downloadable/ for databases.

Obtain a suitable database and place it somewhere on your system;
I suggest `/usr/local/share/GeoIP/`.  Then edit the script to make 
it open the database file (see line 7).

That's it.. enjoy!
