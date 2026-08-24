Personal package archives (PPAs) for the Xiaomi Pad 5 tablet (codename: nabu)
and the OnePlus Pad 3 tablet (codename: erhai).

## Usage

Import the signing key (once):

    wget -qO- https://themojoman.github.io/ppa/themojoman.gpg \
      | sudo gpg --dearmor -o /etc/apt/keyrings/themojoman.gpg

### OnePlus Pad 3 (erhai)

/etc/apt/sources.list.d/oneplus-erhai.sources:

    ## TheMojoMan PPA – OnePlus Pad 3 (erhai)
    Types: deb
    URIs: https://themojoman.github.io/ppa/oneplus-erhai/ubuntu/main/
    Suites: ./
    Signed-By: /etc/apt/keyrings/themojoman.gpg

### Xiaomi Pad 5 (nabu)

/etc/apt/sources.list.d/xiaomi-nabu.sources:

    ## TheMojoMan PPA – Xiaomi Pad 5 (nabu)
    Types: deb
    URIs: https://themojoman.github.io/ppa/xiaomi-nabu/ubuntu/main/
    Suites: ./
    Signed-By: /etc/apt/keyrings/themojoman.gpg

Then: sudo apt update

Note the trailing slash on the URIs and `Suites: ./` — apt resolves the
Release files directly inside the suite folder. A classic one-line
`deb <uri> <suite> main` entry also works via the `dists/<suite>` symlinks.

