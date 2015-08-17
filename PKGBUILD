# Maintainer: Anton Butanaev <anton.butanaev@gmail.com>
pkgname=perwindowlayoutd
pkgver=0.6
pkgrel=2
epoch=
pkgdesc="Keeps per window keyboard layout under X11"
arch=('i686' 'x86_64')
url="https://sourceforge.net/projects/perwindowlayout/"
license=('GPL')
groups=()
depends=(libx11)
makedepends=(gcc)
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=(http://master.dl.sourceforge.net/project/perwindowlayout/$pkgname-$pkgver.tar.gz)
noextract=()
md5sums=(5a0172bf1351e1de2dc3c29363859550)

build() {
  tar xvzf $pkgname-$pkgver.tar.gz
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
