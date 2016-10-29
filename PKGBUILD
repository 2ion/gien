pkgname=gien
pkgver=0.3.1
pkgrel=1
pkgdesc="Export Github issue tracker and wiki contents to local email storage"
arch=('any')
license=('GPL')
url="https://github.com/2ion/gien"
depends=(\
  'python'\
  'python-markdown'\
  'python-progressbar'\
  'python-pygithub'\
  'python-pygit2')
makedepends=('cython' 'pkg-config' 'gcc')
options=(!emptydirs)
source=('https://github.com/2ion/gien/archive/master.tar.gz')
sha256sums=(SKIP)

build()
{
  cd "$srcdir/${pkgname}-master"
  make
}

package()
{
  cd "$srcdir/${pkgname}-master"
  make DESTDIR="$pkgdir/" install
}

