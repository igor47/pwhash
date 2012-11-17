# pwhash #

pwhash is a command-line implementation of the [Web Password Hashing][] algorithm from the [Stanford Security Lab][].

[Web password hashing]: http://crypto.stanford.edu/PwdHash
[Standford Security Lab]: http://seclab.stanford.edu/

## Installation ##

This project depends on the [Rhino][] javascript interpreter.
Most systems can use install [Rhino][] via their local package manager:

On linux: `sudo apt-get install rhino`

On OSX using [brew][]: `brew install rhino`

We also recommend symlinking the binary here to your local bin in your `PATH`:
```bash
  ln -s ./pwhash ~/bin/
```

[Rhino]: https://developer.mozilla.org/en-US/docs/Rhino
[brew]: http://mxcl.github.com/homebrew/

## Usage ##

```bash
pwhash (domain-name)
```

You will be prompted for the domain name (if you didn't specify it on the command line) and the password.

## Rationale ##

You should really use a unique password for every website.
But this is hard for many reasons:

* Nobody can remember a thousand different passwords
* Storing those passwords in a file makes you vulnerable to theft of the file
* Using a password manager makes you dependent on the password manager

The solution is password hashing.
A *unique* password for each website is *generated algorithmically* using your *seed password* and the *domain name* of the site.

## In-Browser Implementations ##

There are a number of in-browser implementations available from the [pwhash website][].
As a last resort, you can always get your password using the in-browser JS tool at that site.

[pwhash website]: https://www.pwdhash.com/
