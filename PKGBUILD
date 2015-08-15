# Maintainer: Holden Cox <segrived@gmail.com>
pkgname=ftjerm
pkgver=0.12.3
pkgrel=1
pkgdesc="Quake-like terminal emulator, a fork of stjerm"
arch=('i686' 'x86_64')
url=('https://github.com/segrived/ftjerm')
license=('GPLv2')
depends=('vte>=0.16' 'gtk2>=2.10')
makedepends=('pkg-config')
source=(${pkgname}-${pkgver}.tar.gz::https://github.com/segrived/ftjerm/tarball/$pkgname-$pkgver)
md5sums=('d850b1bf66bc10e1c889a2a424531488')

build() {
    cd $srcdir/*-$pkgname-*
    make
}

package() {
    cd $srcdir/*-$pkgname-*
    make DESTDIR="$pkgdir/" install
    install -D -m644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}