pkgname=bind-dyndb-ldap
pkgver=11.6
pkgrel=1
pkgdesc='LDAP driver for BIND'
arch=('x86_64')
url=https://pagure.io/bind-dyndb-ldap
license=('GPLv2')
depends=('bind')
makedepends=()
source=("https://releases.pagure.org/bind-dyndb-ldap/$pkgname-$pkgver.tar.bz2")
sha512sums=('e44ee7870aec9304c3d553181392ee2dca38352620bab2f78405aa714a60434990db7fce3a0f1db457257e68bf10fc8a7c23328aee67e7bd5dcda4b8aa67e08c')

build() {
        cd $srcdir/$pkgname-$pkgver
        autoreconf -fvi
        ./configure --prefix=/usr
        make
}

package() {
        cd $srcdir/$pkgname-$pkgver
        make DESTDIR="$pkgdir" install
}
