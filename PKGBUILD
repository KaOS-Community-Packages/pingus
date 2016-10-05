pkgname=pingus
pkgver=0.7.6
pkgrel=2
pkgdesc="A puzzle game where the player has to guide a group of penguins to safety"
url="https://github.com/Pingus/pingus"
arch=('x86_64')
license=('GPL')
depends=('sdl' 'sdl_image' 'sdl_mixer' 'boost' 'boost-libs' 'libpng')
makedepends=('scons')
source=("https://github.com/Pingus/pingus/archive/v${pkgver}.tar.gz")
md5sums=('8f366e7ba76c9f3525888efe8b04b1ad')

build() {
    cd ${srcdir}/${pkgname}-${pkgver}
    scons prefix=/usr
    make
}

package() {
  cd ${srcdir}/${pkgname}-${pkgver}
  make install DESTDIR="${pkgdir}" PREFIX="/usr"
}
