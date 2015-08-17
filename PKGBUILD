# Contributor: Andrea Agosti <cifvts at gmail.com>

pkgname=radlib
pkgver=2.12.0
pkgrel=2
pkgdesc="radlib is a C language library developed to abstract details of interprocess communications and common linux/unix system facilities so that application developers can concentrate on application solutions."
arch=('i686' 'x86_64')
url="http://www.radlib.teel.ws/"
depends=('sqlite')
makedepends=('sqlite')
license=('BSD')
source=(http://downloads.sourceforge.net/radlib/$pkgname-$pkgver.tar.gz)
md5sums=('1330d46ab22e43425169d7dc75f5f2ea')

build() {
	cd ${srcdir}/${pkgname}-${pkgver}
	./configure --prefix=/usr --enable-sqlite
	make || return 1
}
package() {
	cd ${srcdir}/${pkgname}-${pkgver}
	make DESTDIR=$pkgdir install 
}
