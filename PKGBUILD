# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=nscd-s6serv
pkgver=0.1
pkgrel=1
pkgdesc="nscd service for s6"
arch=(x86_64)
license=('beerware')
depends=('glibc' 's6' 's6-rc' 's6-boot')
conflicts=()
install=nscd-s6serv.install
source=('nscd.daemon.finish.s6'
		'nscd.daemon.run.s6'
		'nscd.log.run.s6'
		'LICENSE')
md5sums=('ffee964558d661772df44588409b56f8'
         '5b10688dd4e29e7ca6bcfa1f5ad20d65'
         'be5d0d808347992bff2652b9e2813054'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/nscd.daemon.finish.s6" "$pkgdir/etc/s6-serv/available/classic/nscd/finish"
	install -Dm 0755 "$srcdir/nscd.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/nscd/run"
	
	# log
	install -Dm 0755 "$srcdir/nscd.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/nscd/log/run"
	
	install -Dm 0755 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/nscd-s6serv/LICENSE"
}
