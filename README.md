# Fast FITS Cutter
Fast FITS Cutter makes cutouts of FITS images. FITS I/O goes through the pure-Rust [`fitsio-pure`](https://crates.io/crates/fitsio-pure) crate, so no CFITSIO installation is needed.

## Installation
Clone the repository and run

```bash
cargo build --release
cargo install --path .
```

## Usage

```
 Usage: ffc [OPTIONS] --size <SIZE> <FITSIMAGE> 
 Arguments:
  <FITSIMAGE>  Input image to make a cutout out of

Options:
      --ra <RA>                    Right ascension to centre cutout on [default: 0.0]
      --dec <DEC>                  Declination to centre cutout on [default: 0.0]
      --size <SIZE>                Size of the cutout in degrees
      --outfile <OUTFILE>          Name of the output file [default: output]
      --sourcetable <SOURCETABLE>  CSV table to read cutout positions from. Should contain three columns with name, right ascension and declination [default: ]
  -h, --help                       Print help
  -V, --version                    Print version
```
