# Maintainer: Philipp Schmitt (philipp<at>schmitt<dot>co)

pkgname=pia-tools
pkgver=0.9.6
pkgrel=1
pkgdesc='OpenVPN hook for privateinternetaccess.com'
arch=('any')
url='https://github.com/pschmitt/pia-tools'
license=('GPL3')
depends=('transmission-cli' 'dnsutils' 'openvpn' 'systemd' 'sudo' 'wget' 'ufw' 'unzip' 'sed')
source=('https://raw.github.com/pschmitt/pia-tools/master/pia-tools'
        'https://raw.github.com/pschmitt/pia-tools/master/pia-tools.groff'
        'https://raw.github.com/pschmitt/pia-tools/master/pia@.service'
        'https://raw.github.com/pschmitt/pia-tools/master/pia_common'
        'https://raw.github.com/pschmitt/pia-tools/master/pia-up'
        'https://raw.github.com/pschmitt/pia-tools/master/pia-down'
        'https://raw.github.com/pschmitt/pia-tools/master/pia-tools.install')
sha256sums=('abaf77383286fe6c72450ede5d29e191454570ca926258536fdfe8f1b92f1cf9'
            '35ddc09ca81f1667653d0809cf4fc9b515ce5cfd0011cb3bd6bfa1cc69a3fc03'
            '118d961db36fb243e059543215a818d1546ec94e8d52b24c75b7de6fe64ba749'
            'b571a8edbd9cb2a9ad63fadf360f64d4f80e291295f6c851b3a716c291ba3f8d'
            '20a144766df157988e7f055e2bea11e5decd66fd490f6b516fcbd75140ebb14c'
            '20a144766df157988e7f055e2bea11e5decd66fd490f6b516fcbd75140ebb14c'
            'a7e82a1589406477898adee768d17c0270c8bcf341ae72be823095331c4e99c5')
install="${pkgname}.install"

package() {
    cd "${srcdir}"
    install -Dm755 pia-tools "${pkgdir}/usr/bin/pia-tools"
    install -Dm644 pia-tools.groff "${pkgdir}/usr/share/man/man1/pia-tools.1"
    install -Dm644 pia@.service "${pkgdir}/usr/lib/systemd/system/pia@.service"
    install -Dm644 pia_common "${pkgdir}/etc/openvpn/pia/pia_common"
    install -Dm755 pia-up "${pkgdir}/etc/openvpn/pia/pia-up"
    install -Dm755 pia-up "${pkgdir}/etc/openvpn/pia/pia-down"
}

