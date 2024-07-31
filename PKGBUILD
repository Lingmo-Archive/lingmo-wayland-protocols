pkgname=lingmo-wayland-protocols
pkgver=1.13.0
pkgrel=1
pkgdesc='Lingmo OS Specific Protocols for Wayland'
arch=(any)
url='https://github.com/LingmoOS/lingmo-wayland-protocols'
license=(LGPL-2.0-or-later)
depends=()
makedepends=(extra-cmake-modules
             qt6-base)
source=(git+$url)
sha256sums=('SKIP')
validpgpkeys=('41EF7182553A87AC18196A77F27F2FDA54F067D8') # Lingmo OS Team <team@lingmo.org>

build() {
  cmake -B build -S $pkgname
  cmake --build build -j12
}

package() {
  DESTDIR="$pkgdir" cmake --install build
}

