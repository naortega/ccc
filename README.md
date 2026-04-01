# Catechism CLI (ccc)

A command-line tool for querying sections of the Catechism of the Catholic
Church from the Vatican's website by section number.

## Usage

Before using `ccc` you must first load a cache of where each section is located
on the web.

```bash
ccc --load-cache
# or
ccc -l
```

Once loaded you can query any particular section by simply using the section
number.

```console
$ ccc 241
241 For this reason the apostles confess Jesus to be the Word: "In the beginning was the Word, and the Word was with God, and the Word was God"; as "the image of the invisible God"; as the "radiance of the glory of God and the very stamp of his nature".65
```

Alternatively you can also specify a range of sections to query.

```console
$ ccc 232-233
232 Christians are baptized "in the name of the Father and of the Son and of the Holy Spirit"53 Before receiving the sacrament, they respond to a three-part question when asked to confess the Father, the Son and the Spirit: "I do." "The faith of all Christians rests on the Trinity."54
233 Christians are baptized in the name of the Father and of the Son and of the Holy Spirit: not in their names,55 for there is only one God, the almighty Father, his only Son and the Holy Spirit: the Most Holy Trinity.
```

## Dependencies

The script requires the following Perl modules:

- `LWP::UserAgent` - For HTTP requests
- `JSON::PP` - For JSON parsing
- `File::Spec` - For file path operations
- `File::HomeDir` - For home directory detection
- `File::Path` - For creating cache directory structures
- `Math::Base36` - For calculating the name of the HTML files

The `Math::Base36` module is not a part of standard Perl distribuitions, but can
be installed with [cpan](https://www.cpan.org/modules/INSTALL.html).

## Licensing

This project is licensed under the terms & conditions of the Zlib license. See
the [license file](LICENSE) for more information.
