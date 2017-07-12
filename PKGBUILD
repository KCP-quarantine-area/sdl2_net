pkgname=sdl2_net
epoch=1
pkgver=2.0.1
pkgrel=1
pkgdesc="A small sample cross-platform networking library (Version 2)"
arch=('x86_64')
url="http://www.libsdl.org/projects/SDL_net"
license=('MIT')
depends=(sdl2)
source=("https://www.libsdl.org/projects/SDL_net/release/SDL2_net-${pkgver}.tar.gz")
sha512sums=('d27faee3cddc3592dae38947e6c1df0cbaa95f82fde9c87db6d11f6312d868cea74f6830ad07ceeb3d0d75e9424cebf39e54fddf9a1147e8d9e664609de92b7a')

build() {
  cd "${srcdir}/SDL2_net-${pkgver}/"

  ./configure --disable-static --prefix=/usr
  make
}

package() {
  cd "${srcdir}/SDL2_net-${pkgver}/"

  make DESTDIR="${pkgdir}" install
  install -Dm644 COPYING.txt "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
