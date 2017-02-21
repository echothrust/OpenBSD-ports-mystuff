# $OpenBSD$

COMMENT =		web based syslog interface with whitelisting

VERSION =		v0.5
DISTNAME =		echofish-${VERSION}
PKGNAME =		echofish-${VERSION:S/-/./g:S/v//}
CATEGORIES=		www sysutils

HOMEPAGE =		http://www.echothrust.com/projects/echofish

MAINTAINER =		George Adamopoulos <gadamo@echothrust.com>

# BSD
PERMIT_PACKAGE_CDROM =	Yes


GH_ACCOUNT =		echothrust
GH_PROJECT =		echofish
GH_TAGNAME =		${VERSION}
#MASTER_SITES =		https://github.com/echothrust/echofish/archive/
#DISTFILES =		${VERSION}${EXTRACT_SUFX}

NO_BUILD =		Yes
NO_TEST =		Yes
PKG_ARCH =		*

MODULES =		lang/php
MODULES +=		databases/mariadb
RUN_DEPENDS =		lang/php/${MODPHP_VERSION},-pdo_mysql

PREFIX =		${VARBASE}/www
INSTDIR =		${PREFIX}/echofish
TINSTDIR =		${TRUEPREFIX}/echofish
SUBST_VARS =		INSTDIR TINSTDIR

do-install:
	install -d -g www -m 460 ${WRKDIST}/htdocs/assets
	cp -Rp ${WRKDIST} ${INSTDIR}

.include <bsd.port.mk>
