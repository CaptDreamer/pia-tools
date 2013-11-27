# Maintainer: Philipp Schmitt (philipp<at>schmitt<dot>co)

pkgname=pia-tools-orig
pkgver=0.9.2
pkgrel=3
pkgdesc='OpenVPN hook for privateinternetaccess.com'
arch=('any')
url='https://github.com/pschmitt/pia-tools'
license=('GPL3')
depends=('transmission-cli' 'openvpn' 'systemd' 'sudo' 'wget' 'curl' 'ufw')
source=('https://raw.github.com/pschmitt/pia-tools/master/pia-tools'
        'https://raw.github.com/pschmitt/pia-tools/master/pia-tools.groff'
        'https://raw.github.com/pschmitt/pia-tools/master/pia@.service'
        'https://raw.github.com/pschmitt/pia-tools/master/pia_common')
sha256sums=('e13f49d14b3e78ff777acff062c1ec1774e1065736dd371fbb67a0356726a30e'
            '5a1ffc5094428d70bb0e19f1cc7eec7544b1ad9154a653f75b64f8ac1aeec867'
            'ca889526b3154f221ec57df982c887c6fd02f5be15310fbe25b14d701d4fa394'
            '326197a42525e640432e6ceb3fd0cfe6bbab2324bc607babaa89fb3c80971828')

package() {
    cd "${srcdir}"
    install -Dm755 pia-tools "${pkgdir}/usr/bin/pia-tools"
    install -Dm644 pia-tools.groff "${pkgdir}/usr/share/man/man1/pia-tools.1"
    install -Dm644 pia@.service "${pkgdir}/usr/lib/systemd/system/pia@.service"
    install -Dm644 pia_common "${pkgdir}/etc/openvpn/pia/pia_common"
}

