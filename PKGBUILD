# Maintainer    : Vilmar Catafesta <vcatafesta@gmail.com>
# description   : Change some settings of an xterm
# depends   	:

name=xtermset
version=0.5.2
release=1
pkgname=xtermset
pkgver=0.5.2
pkgrel=1
arch=('x86_64')
pkgdesc='Change some settings of an xterm'
url='https://github.com/biglinux/xtermset'
license=('GPL')
depends=('')
source=(git+https://github.com/biglinux/xtermset)

prepare() {
	pkgdir=${PKG}
	srcdir=${SRC}
    cd ${pkgname}/${pkgname}-${pkgver}
}

build() {
    cd ${pkgname}/${pkgname}-${pkgver}
    aclocal
    autoconf
	automake --add-missing --copy
    ./configure --prefix=/usr
    make
}

package() {
    cd ${pkgname}/${pkgname}-${pkgver}
    make DESTDIR=${pkgdir} install
}


