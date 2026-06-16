pkgname=python-phonecodes
_name=${pkgname#python-}
pkgver=9.0.0
pkgrel=1
pkgdesc="python-phonecodes ipa conversions"
arch=('any')
url="https://pypi.org/project/${_name}"
provides=(${pkgname})
conflicts=(${pkgname})

_name=${_name//-/_}
source=()
noextract=()
sha256sums=()

build() {
    cd "${startdir}" 
    python -m build --wheel --no-isolation 
}

package() {
    cd "${startdir}"
    python -m installer --destdir="${pkgdir}" dist/*.whl 
}
