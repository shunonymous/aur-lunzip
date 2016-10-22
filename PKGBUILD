# Maintainer: Shun Terabayashi <shunonymous@gmail.com>

pkgname=lunzip
pkgver=1.8
pkgrel=1
pkgdesc="A decompressor for lzip files."
arch=('i686' 'x86_64')
url="http://www.nongnu.org/lzip/lunzip.html"
license=('GNU GPL v2')
source=(https://download.savannah.gnu.org/releases/lzip/lunzip/$pkgname-$pkgver.tar.gz)
noextract=()
md5sums=('fcad8f8c42a43234b777951b9c6e6684')

prepare() {
  cd "$srcdir/$pkgname-$pkgver"
}

build() {
  cd "$srcdir/$pkgname-$pkgver"

  ./configure --prefix=/usr
  make
}

check() {
  cd "$srcdir/$pkgname-$pkgver"

  make -k check
}

package() {
  cd "$srcdir/$pkgname-$pkgver"

  make DESTDIR="$pkgdir/" install
}

# vim:set ts=2 sw=2 et:
