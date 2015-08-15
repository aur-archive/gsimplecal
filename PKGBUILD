# Maintainer: jsteel <mail at jsteel dot org>
# Contributor: DrZaius <lou at fakeoutdoorsman dot com>
# Contributor: Victor Feight <vrfeight3 at gmail dot com>

pkgname=gsimplecal
pkgver=1.6
pkgrel=1
pkgdesc="Simple and lightweight GTK calendar"
arch=('i686' 'x86_64')
url="http://dmedvinsky.github.com/$pkgname"
license=('BSD')
depends=('gtk2')
source=(https://github.com/downloads/dmedvinsky/$pkgname/$pkgname-$pkgver.tar.gz)
md5sums=('05a596de37491e52b646a0c71ec14841')

build() {
  cd "$srcdir"/$pkgname-$pkgver

  ./configure --prefix=/usr

  make
}

package() {
  cd "$srcdir"/$pkgname-$pkgver

  make DESTDIR="$pkgdir" install

  install -Dm644 COPYING "$pkgdir"/usr/share/licenses/$pkgname/LICENSE
}
