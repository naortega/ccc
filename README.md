# Catechism CLI (ccc)

A command-line tool for querying sections of the Catechism of the Catholic
Church by section number.

## Usage

```bash
ccc <section_number>
```

## Dependencies

The script requires the following Perl modules (all included in standard Perl
distributions):

- `LWP::UserAgent` - For HTTP requests
- `JSON::PP` - For JSON parsing
- `File::Spec` - For file path operations
- `File::HomeDir` - For home directory detection
- `File::Path` - For creating cache directory structures

## Licensing

This project is licensed under the terms & conditions of the Zlib license. See
the [license file](LICENSE) for more information.
