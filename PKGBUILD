# Contributor: das-ich <das-ich at yandex.ru>

pkgname=knutclient
pkgver=1.0.5
pkgrel=7
pkgdesc="Knutclient is a GUI interface for UPS system NUT."
#url="http://www.knut.noveradsl.cz/knutclient/"
url="http://kde-apps.org/content/show.php/KNutClient?content=44259"
arch=('i686' 'x86_64')
license=('GPL')
depends=("kdelibs" "qt4")
makedepends=('cmake' 'automoc4')
source=(http://knut.googlecode.com/files/$pkgname-$pkgver.tar.gz)
md5sums=('f98ec9684fea7585d4be089c8313c894')

build() {
  cd $srcdir/knc105
  cd build
  cmake ../. -DCMAKE_INSTALL_PREFIX=/usr/ -DCMAKE_BUILD_TYPE=Release
  make || return 1
#  make DESTDIR=$startdir/pkg install
}
package() {
  cd $srcdir/knc105
  cd build
  make DESTDIR="$pkgdir" install
}