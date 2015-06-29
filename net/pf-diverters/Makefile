# $OpenBSD: Makefile.template,v 1.71 2014/07/10 12:33:17 sthen Exp $
COMMENT =		collection of divert socket deamons for PF
CATEGORIES =		net
HOMEPAGE =		https://www.echothrust.com/projects/pf-diverters
MAINTAINER = 		Pantelis Roditis <proditis@echothrust.com>	
PERMIT_PACKAGE_CDROM =	Yes

DISTNAME =      	${GH_PROJECT}-${GH_TAGNAME}
GH_ACCOUNT =		echothrust
GH_TAGNAME =		5.7p0
GH_PROJECT =		pf-diverters
GH_COMMIT =			5c347c8e3c3e7daab221c9165b5e16717e08bcaf

EXTRACT_SUFX =		.tar.gz


do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/bofh/bofh-divert ${PREFIX}/sbin
	${INSTALL_PROGRAM} ${WRKSRC}/dnsbl/dnsbl-divert ${PREFIX}/sbin
	${INSTALL_DATA_DIR} ${PREFIX}/share/examples/pf-diverters
	${INSTALL_DATA} ${WRKSRC}/README.md   \
		${PREFIX}/share/examples/pf-diverters/README.md
	${INSTALL_DATA} ${WRKSRC}/rc.bofh   \
		${PREFIX}/share/examples/pf-diverters/bofh_divert
	${INSTALL_DATA} ${WRKSRC}/rc.dnsbl   \
		${PREFIX}/share/examples/pf-diverters/dnsbl_divert


.include <bsd.port.mk>
