# Maintainer: Mikołaj Baranowski <mikolajb@gmail.com>

pkgname=uva-vpn
pkgver=20131024
pkgrel=1
pkgdesc='Archlinux package for the University of Amsterdam VPN software'
license=('custom')
depends=('lib32-glibc'
         'lib32-zlib'
         'net-tools')
arch=('x86_64' 'i686')
url='http://staff.uva.nl/a-z/content/working-from-home-uva-vpn/working-from-home-uva-vpn.html'
source=('linux-vpn-installer-redhat-based-systemen.rpm'
        'certificaat-uvavpn.der')
md5sums=('d18d28044ee7e8a95dffc0048f780bad'
         '40f1a2e4044897f018e63d3790ed3d43')

package() {
  msg2 'Installing...'

  install -Dm644 "$srcdir/usr/local/nc/libncui.so" "${pkgdir}/usr/local/nc/libncui.so"
  install -m644 "$srcdir/usr/local/nc/NC.jar" "${pkgdir}/usr/local/nc/NC.jar"
  install -m644 "$srcdir/usr/local/nc/version.txt" "${pkgdir}/usr/local/nc/version.txt"
  install -m644 "$srcdir/certificaat-uvavpn.der" "${pkgdir}/usr/local/nc/certificaat-uvavpn.der"
  install -m755 "$srcdir/usr/local/nc/ncdiag" "${pkgdir}/usr/local/nc/ncdiag"
  install -m755 "$srcdir/usr/local/nc/ncsvc" "${pkgdir}/usr/local/nc/ncsvc"
}
