# Contributor: Hubert CzobodziÅ„ski <hcz@onet.eu>
pkgname=plr
pkgver=8.3.0.14
pkgrel=1
pkgdesc="PL/R - R procedural language for PostgreSQL"
arch=('i686' 'x86_64')
url="http://www.joeconway.com/plr"
license=('GPL')
depends=('postgresql>=8.4' 'r')
source=(http://www.joeconway.com/plr/${pkgname}-${pkgver}.tar.gz)
md5sums=('f71ff392be1ff584a5f66b06d5f83b00')

build() {
  cd ${startdir}/src/${pkgname}
  export USE_PGXS=1
  make || return 1
  make DESTDIR=${startdir}/pkg install || return 1
}
