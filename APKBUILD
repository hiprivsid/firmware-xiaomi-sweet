pkgname=firmware-xiaomi-sweet
pkgver=1
pkgrel=0
_commit="9d78c9f9b0c8e644c8a2d0f575cd35f2d0b7ff5a"
pkgdesc="Firmware files for Xiaomi Redmi Note 10 Pro"
url="https://postmarketos.org"
arch="aarch64"
license="proprietary"
depends="wcnss-wlan adsp-audio"
source="$_commit.tar.gz::https://github.com/hiprivsid/postmarketos-vendor-xiaomi-sweet/archive/$_commit.tar.gz"
options="!strip !check !archcheck !spdx !tracedeps pmb:cross-native"

_fwdir="/lib/firmware/postmarketos"

package() {
	cd "$srcdir/postmarketos-vendor-xiaomi-sweet-$_commit"

	# ADSP firmware
	install -Dm0644 adsp/adsp.* -t "$pkgdir/$_fwdir"

	# Fingerprint firmware
	# i don't have it

	# GPU and video acceleration firmwares
	install -Dm0644 gpu/a6* -t "$pkgdir/$_fwdir/../qcom"
  install -Dm0644 gpu/a702* -t "$pkgdir/$_fwdir/../qcom"
	install -Dm0644 gpu/*_zap.* -t "$pkgdir/$_fwdir"

	# Modem firmware
	install -Dm0644 modem/modem.* -t "$pkgdir/$_fwdir"

	# Wifi/BT firmware
  # i don't have it
}

sha512sums=""
