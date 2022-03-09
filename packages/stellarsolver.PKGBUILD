pkgname=stellarsolver
pkgver=1.9
pkgrel=2
pkgdesc='The cross platform Sextractor and Astrometry.net-Based internal astrometric solver'
arch=(x86_64 aarch64)
url='https://github.com/rlancaste/stellarsolver'
license=(GPL3)
depends=(qt5-base gsl wcslib)
makedepends=(cmake)
source=(https://github.com/rlancaste/stellarsolver/archive/$pkgver/$pkgname-$pkgver.tar.gz)
sha256sums=('e7f6c212da981556ea2a64f131a5f2549a9d098669082ef076ec3230bbfefb66')

build() {
  cmake -B build -S $pkgname-$pkgver \
    -DCMAKE_INSTALL_PREFIX=/usr
  cmake --build build
}

package() {
  DESTDIR="$pkgdir" cmake --install build
}
