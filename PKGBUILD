# Original Maintainer: gobonja <gobonja@gmail.com>
# Maintainer: Calliope System <calliopesystem@gmail.com>

pkgname=timeshift-autosnap-git
_pkgname=timeshift-autosnap
pkgver=1.0
pkgrel=1
pkgdesc="Timeshift auto-snapshot script which runs before package upgrade using Pacman hook."
arch=("any")
url="https://github.com/CalliopeSystem/timeshift-autosnap.git"
license=('MIT')
depends=('timeshift')
optdepends=('grub-btrfs')
provides=('timeshift-autosnap')
source=(git+${url})
backup=('etc/timeshift-autosnap.conf')
md5sums=('SKIP')

package() {
    cd ${srcdir}/${_pkgname}
    install -Dm644 00-timeshift-autosnap.hook ${pkgdir}/usr/share/libalpm/hooks/00-timeshift-autosnap.hook
    install -Dm644 timeshift-autosnap.conf ${pkgdir}/etc/timeshift-autosnap.conf
    install -Dm755 timeshift-autosnap ${pkgdir}/usr/bin/timeshift-autosnap
    install -Dm644 LICENSE ${pkgdir}/usr/share/licenses/${pkgname}/LICENSE
}
