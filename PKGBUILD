pkgname=virtualmoon6
pkgver=6.0
pkgrel=1
pkgdesc="Virtual Moon Atlas - free software for Moon observation or survey"
pkgext='.pkg.tar'
arch=('i686' 'x86_64')
license=('GPL')
depends=('gtk2')
url="http://www.ap-i.net/avl/en/start"
# needs ~15GB to create package
# When this package expires, will change Version%206.0 to old%20Version%206.0 in line below
source=(http://iweb.dl.sourceforge.net/project/virtualmoon/1-%20virtualmoon/Version%206.0/Linux/virtualmoon-6.0-linux.tar
	###Extra textures###
	#LRO WAC High resolution 250m/pixel - 155 MB
	http://prdownloads.sourceforge.net/virtualmoon/TexturesWAC.tgz
	#LRO WAC High resolution 120m/pixel - 375 MB
	http://prdownloads.sourceforge.net/virtualmoon/TexturesWAC_L5.tgz
	#Chang'e 2 High resolution 250m/pixel - 138 MB
	http://prdownloads.sourceforge.net/virtualmoon/TexturesChange.tgz
	#Chang'e 2 High resolution 120m/pixel -343 MB
	http://prdownloads.sourceforge.net/virtualmoon/TexturesChange_L5.tgz
	#Chang'e 2 High resolution 60m/pixel - 1.2 GB
	http://prdownloads.sourceforge.net/virtualmoon/TexturesChange_L6.tgz
        #Historical maps - 27MB
	http://prdownloads.sourceforge.net/virtualmoon/TextureHistorical.tgz
	#High res Clementine photographic textures - 125 MB
	http://prdownloads.sourceforge.net/virtualmoon/TexturesClementine.tgz
	#High res Lunar Orbiter photgraphic texture - 166 MB 250m/pixel
	http://prdownloads.sourceforge.net/virtualmoon/TexturesLopam.tgz
	#High res Lunar Orbiter photographic texture - 303 MB 120m/pixel
	http://prdownloads.sourceforge.net/virtualmoon/TexturesLopam_L5.tgz
	#High resolution Lunar Orbiter photographic texture 60m/pixel  - 1 GB
	http://prdownloads.sourceforge.net/virtualmoon/TexturesLopam_L6.tgz
	#Airbrush without albedo texture - 40 MB
	http://prdownloads.sourceforge.net/virtualmoon/TexturesAirbrush_na.tgz
	###Pictures library###
	#BEST OF DAMIAN PEACH - 55 MB
	http://prdownloads.sourceforge.net/virtualmoon/PictureBest_of_Peach.tgz
	#BEST OF PIC DU MIDI - 12 MB
	http://prdownloads.sourceforge.net/virtualmoon/PictureBest_Pic_du_Midi.tgz
	#Best of amateurs - 27 MB
	http://prdownloads.sourceforge.net/virtualmoon/PictureBestOfAmateurs.tgz
	#Lunar Orbiter photographic atlas of the moon (LOPAM) - 25 MB, 5.1 MB
	http://prdownloads.sourceforge.net/virtualmoon/PictureLopam.tgz
	http://prdownloads.sourceforge.net/virtualmoon/PictureLunaStars.tgz
	#Apollo mapping cameras - 40 MB
	http://prdownloads.sourceforge.net/virtualmoon/PictureApolloMapping.tgz
	#Lunar astronautical charts and lunar maps - 62 MB
	http://prdownloads.sourceforge.net/virtualmoon/PictureLAC_LM.tgz
	#Consolidated lunar atlas - 85 MB
	http://prdownloads.sourceforge.net/virtualmoon/PictureCLA.tgz
	#Apollo missions - 9.5 MB
	http://prdownloads.sourceforge.net/virtualmoon/PictureApollo.tgz
	#Luna, Ranger, Lunar Orbiter 1, 2, 3, 5 and Surveyor probes - 5 MB
	http://prdownloads.sourceforge.net/virtualmoon/PictureProbes.tgz
	#Clementine probe - 4.2 MB
	http://prdownloads.sourceforge.net/virtualmoon/PictureClementine.tgz
	#Kaguya probe - 15 MB
	http://prdownloads.sourceforge.net/virtualmoon/PictureKaguya.tgz)
sha1sums=('b5c74aaec529a880e590191bca769710a2e0024b'
	  'b301b9c42e65b90fc1ee697c4fbdc4a6fbd5b092'
	  '6a2de224b46c624abb199a952fadd738a7825abc'
	  'e4498a4b6fd42db0efcc8b39bb13662d1d02aae2'
	  '2a87e635ae497181d90bb4bacc78f42b4c151629'
	  '7bd5d8c161da041da7463225a7e7b3a5238c21c9'
	  '38ea3ddbce78088b6b048e808d6fc3fb5a68b3fd'
	  '91dcd836df110e2222703b4bf44c07843a9d27fc'
	  '3a6e18a4b461a0b3cf1ff97f7522be05a5b0e2b3'
	  '68352a19b1b5d628ec6d6813c33dfd9731984ef5'
	  'da3cf63c4fdc1e4b5e6c588de4190be327258c22'
      	  'df7abc9ebcc436f957e23feed9c4a2f1f846dadf'
	  '7bb4e59111ccf7ac4f02a5ade55023059b5863cf'
	  '341cb7307d48438a64aae77516921439248de1eb'
	  'd3e05ada36bcef6c232a333f3e054112b428e979'
	  '07e27e707a174b1b1f045a0aaaa097e926b9f43e'
	  'a49c85f0d9701de3d9f45dc631a2212c5abcfe82'
	  'bef05fef2f2616383cfc8f161cbf27f469ee3c4c'
	  '8ab41fdb2025b684ab6dab7995b91f8399deaeb4'
	  '95ece23d207ead5752301b37bdae377402be35b1'
	  '5d80d52243bb9a6e1ddad579ce1370c379a4af3a'
	  '449fb60545e4b487cab4bd67d61b128ee120bdc3'
	  '40b50b615f6ff2fa4f98bc1d197907d9bcf24b73'
	  '50baf21c538d477bbc3f9f057e2e2d0278c80d4d'
)
package() {
	tar xf ${srcdir}/virtualmoon-$pkgver-linux.tar
	mkdir ${pkgdir}/usr/
if [[ "$CARCH" == 'i686' ]]; then
	tar xvzf ${srcdir}/virtualmoon-$pkgver-linux_i386.tgz -C ${pkgdir}/usr/
else
	tar xvzf ${srcdir}/virtualmoon-$pkgver-linux_x86_64.tgz -C ${pkgdir}/usr/
fi
	tar xvzf ${srcdir}/virtualmoon-data-$pkgver-linux_all.tgz -C ${pkgdir}/usr/

###Extra textures#### 

#LRO WAC High resolution 250m/pixel - 155 MB
tar xzvf ${srcdir}/TexturesWAC.tgz -C ${pkgdir}/usr/

#LRO WAC High resolution 120m/pixel - 375 MB
tar xzvf ${srcdir}/TexturesWAC_L5.tgz -C ${pkgdir}/usr/

#Chang'e 2 High resolution 250m/pixel - 138 MB
tar xzvf ${srcdir}/TexturesChange.tgz -C ${pkgdir}/usr/

#Chang'e 2 High resolution 120m/pixel - 343 MB
tar xzvf ${srcdir}/TexturesChange_L5.tgz -C ${pkgdir}/usr/

#Chang'e 2 High resolution 60m/pixel - 1.2 GB
tar xzvf ${srcdir}/TexturesChange_L6.tgz -C ${pkgdir}/usr/

#Historical maps - 27MB
tar xzvf ${srcdir}/TextureHistorical.tgz -C ${pkgdir}/usr/

#High res Clementine photographic textures - 125 MB
tar xzvf ${srcdir}/TexturesClementine.tgz -C ${pkgdir}/usr/

#High res Lunar Orbiter photgraphic texture - 166 MB 250m/pixel
tar xzvf ${srcdir}/TexturesLopam.tgz -C ${pkgdir}/usr/

#High res Lunar Orbiter photographic texture - 303 MB 120m/pixel
tar xzvf ${srcdir}/TexturesLopam_L5.tgz -C ${pkgdir}/usr/

#High res Lunar Orbiter photographic texture - 1 GB 60m/pixel
tar xzvf ${srcdir}/TexturesLopam_L6.tgz -C ${pkgdir}/usr/

#Airbrush without albedo texture - 40 MB
tar xzvf ${srcdir}/TexturesAirbrush_na.tgz -C ${pkgdir}/usr/

###Pictures library###

#BEST OF DAMIAN PEACH - 55 MB
tar zxvf ${srcdir}/PictureBest_of_Peach.tgz -C ${pkgdir}/usr/

#BEST OF PIC DU MIDI - 12 MB
tar zxvf ${srcdir}/PictureBest_Pic_du_Midi.tgz -C ${pkgdir}/usr/

#Best of amateurs -27 MB
tar xzvf ${srcdir}/PictureBestOfAmateurs.tgz -C ${pkgdir}/usr/

#Lunar Orbiter photographic atlas of the moon (LOPAM) - 25 MB, 5.1 MB
tar xzvf ${srcdir}/PictureLopam.tgz -C ${pkgdir}/usr/
tar xzvf ${srcdir}/PictureLunaStars.tgz -C ${pkgdir}/usr/

#Apollo mapping cameras - 40 MB
tar xzvf ${srcdir}/PictureApolloMapping.tgz -C ${pkgdir}/usr/

#Lunar astronautical charts and lunar maps - 62 MB
tar xzvf ${srcdir}/PictureLAC_LM.tgz -C ${pkgdir}/usr/

#Consolidated lunar atlas - 85 MB
tar xzvf ${srcdir}/PictureCLA.tgz -C ${pkgdir}/usr/

#Apollo missions - 9.5 MB
tar xzvf ${srcdir}/PictureApollo.tgz -C ${pkgdir}/usr/

#Luna, Ranger, Lunar Orbiter 1, 2, 3, 5 and Surveyor probes - 5 MB
tar xzvf ${srcdir}/PictureProbes.tgz -C ${pkgdir}/usr/

#Clementine probe - 4.2 MB
tar xzvf ${srcdir}/PictureClementine.tgz -C ${pkgdir}/usr/

#Kaguya probe - 15 MB
tar xzvf ${srcdir}/PictureKaguya.tgz -C ${pkgdir}/usr/

}
