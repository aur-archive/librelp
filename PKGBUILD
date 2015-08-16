# Maintainer: Kaiting Chen <kaiting.chen@kiwilight.com>

pkgdesc="The Reliable Event Logging Protocol"
url="http://www.librelp.com/"

pkgname='librelp'
pkgver='1.2.7'
pkgrel='2'
arch=('i686' 'x86_64')
license=('GPL3')

md5sums=('26e02602490af3a681a2a13e6ce29efb')

_source="http://download.rsyslog.com/"
_file="${pkgname}-${pkgver}.tar.gz"
source=("${_source}/${pkgname}/${_file}")

build() {
  cd ${srcdir}/${pkgname}-${pkgver}

  ./configure --prefix=/usr
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make DESTDIR="$pkgdir" install
}
