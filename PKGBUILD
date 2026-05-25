pkgname=kando-haptic
pkgver=0.3
pkgrel=1
pkgdesc="Kando haptic listener for Logitech Master MX4"
arch=('x86_64')
url="https://github.com/Thelenyii/kando-haptic-mx4"

depends=(
    'python'
    'python-websockets'
    'systemd'
)

install="${pkgname}.install"

source=(
    'kando-haptic-mx4'
    'kando-mx4-hid'
    'kando-haptic-mx4@.service'
)

sha256sums=('SKIP' 'SKIP' 'SKIP')

package() {
    install -dm755 "$pkgdir/opt/haptic-kando"

    install -Dm755 kando-haptic-mx4 \
        "$pkgdir/opt/haptic-kando/kando-haptic-mx4"

    install -Dm755 kando-mx4-hid \
        "$pkgdir/opt/haptic-kando/kando-mx4-hid"

    install -Dm644 kando-haptic-mx4@.service \
        "$pkgdir/usr/lib/systemd/system/kando-haptic-mx4@.service"
}
