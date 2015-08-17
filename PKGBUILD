# $Id: PKGBUILD 96067 2013-08-19 19:21:25Z jelle $
# Maintainer: Eric Bélanger <eric@archlinux.org>
# Contributor: Kritoke <kritoke@nospam.gamebox.net>

pkgname=ogle-gui
pkgver=0.9.2
pkgrel=5
pkgdesc="A gtk2 gui for ogle"
arch=('i686' 'x86_64')
url="http://www.dtek.chalmers.se/groups/dvd/"
license=('GPL')
depends=('ogle' 'libglade')
#source=(http://www.dtek.chalmers.se/groups/dvd/dist/ogle_gui-${pkgver}.tar.gz)
source=(ftp://ftp.archlinux.org/other/community/ogle-gui/ogle_gui-${pkgver}.tar.gz)
md5sums=('e685aa3046f9da13532ede9300f2f794')
sha1sums=('0d73ec30852b9cd2a9714b5088f6ab6deecf097d')

build() {
  cd "${srcdir}/ogle_gui-${pkgver}"

  # fix for FS#36235
  export LDFLAGS=" -lX11 $LDFLAGS"
  ./configure --prefix=/usr --enable-gtk2
  make
}

package() {
  cd "${srcdir}/ogle_gui-${pkgver}"
  make DESTDIR="${pkgdir}" install
}
