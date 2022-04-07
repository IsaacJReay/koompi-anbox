pkgname=koompi-anbox
pkgver=2
pkgrel=3
pkgdesc='Anbox in One'
url='http://anbox.io/'
license=('GPL3')
arch=('x86_64')
depends=('anbox-modules-dkms' 'anbox-image-gapps' 'anbox-git' 'lxc-git' 'libcpufeatures-git' 'networkmanager' 'sdbus-cpp' 'linux>=5.17.1.arch1' 'linux-headers')
conflicts=('koompi-linux' 'linux-lts' 'linux-zen' 'acpi_call-koompi-linux')
source=(
	"$pkgname.install" 
	"$pkgname.conf"
)
sha256sums=(
	'c09afa65f99014e2d355e0e28d2750448260b56561a5690c4ad69a12e40d00ff'
	'a4d99b891115e8be58e91deebe4ae73d118810856b8e7accc3ae3b94ed0ac90e'
)
install="$pkgname.install"

package() {
	install -Dm644 "$srcdir/$pkgname.conf" -t "$pkgdir/etc/modules-load.d/"
	install -dm644 "$pkgdir/dev/binderfs"
}
