PKGBUILD: PKGBUILD_ ../.tag.${version}
	perl -pe 's/^\#\#.*$$//; s/^pkgver=xxx$$/pkgver=${version}/;' PKGBUILD_ > PKGBUILD
	makepkg -g >> PKGBUILD

"${pkgname}-${version}-1.src.tar.gz": PKGBUILD
	mkaurball

archlinux: "${pkgname}-${version}-1.src.tar.gz"
	burp -C${HOME}/.config/burp.cookies "${pkgname}-${version}-1.src.tar.gz"
