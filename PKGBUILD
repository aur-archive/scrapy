# Maintainer: PyroDevil <p dot devil at gmail dot com>
# Contributor: Anibal Pacheco <apacheco.uy@gmail.com>
pkgname="scrapy"
pkgver=0.24.6
pkgrel=1
pkgdesc="A fast high-level scraping and web crawling framework."
arch=(any)
license=('BSD')
url="http://scrapy.org"
depends=('twisted>=10.0' 'libxml2>=2.6.28' 'python2-w3lib>=1.8' 
         'python2-lxml' 'python2-six>=1.5.2' 'python2-queuelib' 
         'python2-setuptools' 'python2-cssselect>=0.9'
         'python2-pyopenssl')
makedepends=('git')
optdepends=('ipython2: for enhanced support of the interactive scraping shell')
provides=('scrapy')
conflicts=('scrapy-hg' 'scrapy-git')
options=(!emptydirs)
source=("git+https://github.com/scrapy/scrapy.git#tag=${pkgver}")
md5sums=('SKIP')

package() {
  cd "${srcdir}/scrapy"
  python2 setup.py install --root="${pkgdir}"
  
  # copying license information
  install -D -m644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"

  # copying readme information
  install -D -m644 "README.rst" "${pkgdir}/usr/share/doc/${pkgname}/README.rst"
  install -D -m644 "docs/intro/install.rst" "${pkgdir}/usr/share/doc/${pkgname}/INSTALL.rst"
}
